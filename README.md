import random

# CONFIGURATION
OUTPUT_FILE = "batman-contribution.svg"
COLS = 53
ROWS = 7

# Batman Yellow/Dark Palette
# Level 0 (bg) -> Level 4 (brightest)
COLORS = [
    "#161b22", # 0: Dark Background
    "#21262d", # 1: Slightly lighter (Noise)
    "#475569", # 2: Grey
    "#fbbf24", # 3: Yellow
    "#f59e0b"  # 4: Bright Orange/Yellow
]

# 7-Row Bitmap of Batman Logo (0=Empty, 1=Fill)
BAT_LOGO = [
    [0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0],
    [0,1,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,1,0,0],
    [1,1,1,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,1,1,1,0],
    [1,1,1,1,1,0,0,0,1,1,1,1,0,0,0,1,1,1,1,1,1,0],
    [1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,0],
    [0,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,0,0],
    [0,0,1,1,1,0,0,1,1,1,1,1,1,0,0,1,1,1,0,0,0,0]
]

def generate_svg():
    # Calculate centering
    logo_width = len(BAT_LOGO[0])
    start_col = (COLS - logo_width) // 2
    
    rects = []
    
    for c in range(COLS):
        for r in range(ROWS):
            # Determine Color Level
            level = 0
            
            # Check if we are inside the logo area
            logo_c = c - start_col
            if 0 <= logo_c < logo_width and BAT_LOGO[r][logo_c] == 1:
                # Inside Logo: High intensity (3 or 4)
                level = 4 if random.random() > 0.3 else 3
            else:
                # Outside Logo: Background noise (0 or 1)
                level = 1 if random.random() > 0.9 else 0
                
            color = COLORS[level]
            
            # SVG Geometry
            x = c * 14
            y = r * 14
            rect = f'<rect x="{x}" y="{y}" width="10" height="10" rx="2" ry="2" fill="{color}" />'
            rects.append(rect)

    svg_content = f"""
    <svg width="{COLS * 14}" height="{ROWS * 14}" viewBox="0 0 {COLS * 14} {ROWS * 14}" xmlns="http://www.w3.org/2000/svg">
      <style>
        rect {{ shape-rendering: geometricPrecision; }}
      </style>
      <g transform="translate(0, 0)">
        {''.join(rects)}
      </g>
    </svg>
    """
    
    with open(OUTPUT_FILE, "w") as f:
        f.write(svg_content.strip())
    
    print(f"Generated {OUTPUT_FILE}! You can now upload this to your README.")

if __name__ == "__main__":
    generate_svg()
