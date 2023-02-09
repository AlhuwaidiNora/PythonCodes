# Python code that generates random "abstract" images using the Python Imaging Library (PIL):
import random
from PIL import Image, ImageDraw

# Create a blank image with a white background
img = Image.new("RGB", (500, 500), (255, 255, 255))
draw = ImageDraw.Draw(img)

# Generate random lines and shapes on the image
for i in range(100):
    x1 = random.randint(0, 500)
    y1 = random.randint(0, 500)
    x2 = random.randint(0, 500)
    y2 = random.randint(0, 500)
    line_width = random.randint(1, 10)
    red = random.randint(0, 255)
    green = random.randint(0, 255)
    blue = random.randint(0, 255)
    draw.line((x1, y1, x2, y2), fill=(red, green, blue), width=line_width)

# Save the image
img.save("abstract_art.png")
