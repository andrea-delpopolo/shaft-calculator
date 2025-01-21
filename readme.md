# Spearfishing Shaft Weight Comparison Tool

This project is a simple web-based tool to compare the volume of spearfishing shafts with different diameters and lengths. It helps spearfishers optimize their gear choices by calculating the relative volume increase between shafts.

## Features

- **User-friendly form:** Input default and new shaft dimensions.
- **Automatic calculations:** Compares shaft volumes based on diameter and length.
- **Dynamic table:** Displays results with an option to sort and remove entries.
- **Accessible design:** Includes semantic HTML, ARIA roles, and a responsive layout.
- **SEO-optimized:** Metadata and descriptive content for improved visibility.

## Demo

You can test the tool by opening the `index.html` file in your browser.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/andrea-delpopolo/shaft-comparison-tool.git

## How the calculation works

The volume of a cylindrical object, like a shaft, is calculated using the formula:

\[
\text{Volume} = \pi \times (\text{radius})^2 \times \text{height}
\]

Where:
- \( \pi \) (pi) is approximately 3.14159.
- \( \text{radius} \) is half of the diameter of the cylinder.
- \( \text{height} \) corresponds to the length of the cylinder.

### Conversion Notes
- Convert the diameter to the radius by dividing it by 2:
  \[
  \text{radius} = \frac{\text{diameter}}{2}
  \]
- Convert the length from centimeters to millimeters if needed:
  \[
  \text{length in mm} = \text{length in cm} \times 10
  \]

---

## Example

### Default Shaft
- Diameter: 6.5 mm
- Length: 140 cm

### New Shaft
- Diameter: 7.0 mm
- Length: 130 cm

### Calculation
1. **Default Shaft Volume**:
   \[
   \pi \times (6.5 / 2)^2 \times (140 \times 10)
   \]
2. **New Shaft Volume**:
   \[
   \pi \times (7.0 / 2)^2 \times (130 \times 10)
   \]
3. **Relative Increase (%)**:
   \[
   \text{Increase} = \frac{\text{New Volume} - \text{Default Volume}}{\text{Default Volume}} \times 100
   \]

---

## Features
- **Input Fields**: Enter shaft diameters and lengths to compare.
- **Results Table**: View relative volume changes sorted by percentage increase.
- **Interactive**: Add or remove shafts dynamically.

```html
<script>
    // Example of using the `calculateVolume` function:
    function calculateVolume(diameter, length) {
        const radius = diameter / 2; // Diameter to radius in mm
        const lengthMm = length * 10; // Convert length to mm
        return Math.PI * Math.pow(radius, 2) * lengthMm; // Volume in mm³
    }
</script>

## See it live

[spearfishing-shaft-calculator.netlify.app](https://spearfishing-shaft-calculator.netlify.app/)