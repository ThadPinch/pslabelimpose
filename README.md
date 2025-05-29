# PDF Label Imposition Tool

A web-based tool for imposing PDF labels onto large format sheets for efficient printing. This tool automatically arranges multiple copies of a single PDF label onto a 321mm × 830mm sheet with optimal spacing and registration marks.

## Features

- **Automatic Layout Calculation**: Determines the optimal number of labels that fit on each sheet
- **Smart Rotation**: Automatically rotates labels 90° if it allows more labels per sheet
- **Drag & Drop Interface**: Simply drag your PDF file onto the upload zone
- **CMYK Color Preservation**: Maintains original PDF color spaces and quality
- **Registration Marks**: Adds 0.25" × 0.25" black squares for alignment (one per row)
- **Live Preview**: View the imposed PDF directly in your browser with zoom controls
- **Instant Download**: Automatically downloads the imposed PDF after processing

## How to Use

1. **Open the HTML file** in a modern web browser (Chrome, Firefox, Safari, or Edge)
2. **Upload your PDF** by either:
   - Dragging and dropping it onto the blue upload area
   - Clicking the upload area and selecting your file
3. **View the results** - The tool will display:
   - Original label size
   - Grid layout (columns × rows)
   - Total labels per sheet
   - Whether rotation was applied
4. **Download** - The imposed PDF automatically downloads with "_imposed" added to the filename

## Technical Specifications

### Sheet Size
- Width: 321mm (12.64")
- Height: 830mm (32.68")

### Gap Distribution
- Labels are evenly distributed across the sheet
- Edge margins are half the size of inter-label gaps
- This ensures consistent spacing throughout the layout

### Registration Marks
- Size: 0.25" × 0.25" (6.35mm × 6.35mm)
- Color: 100% K (CMYK black)
- Position: 9.35mm to the left of the leftmost label in each row
- Purpose: Alignment guides for cutting or finishing

### File Handling
- Input: Single-page PDF files (with or without bleed)
- Output: Single-page imposed PDF
- Naming: `original_filename_imposed.pdf`

## Browser Requirements

- Modern browser with JavaScript enabled
- PDF.js library (loaded from CDN)
- PDF-lib library (loaded from CDN)

## Important Notes

- The tool processes only the first page of multi-page PDFs
- Original PDF quality and color spaces are preserved
- All processing happens in your browser - no files are uploaded to any server
- Large files may take a moment to process

## Troubleshooting

**PDF won't upload:**
- Ensure the file is a valid PDF
- Check that JavaScript is enabled in your browser
- Try refreshing the page and uploading again

**Download doesn't start:**
- Check your browser's download settings
- Look for the file in your default downloads folder
- Check the browser console for error messages

**Preview looks incorrect:**
- Try zooming in/out using the zoom controls
- Ensure your PDF doesn't have unusual page sizes or rotations
- Check that the PDF isn't corrupted

## Technical Implementation

The tool uses:
- **PDF-lib** for PDF manipulation and creation
- **PDF.js** for rendering PDF previews
- **Pure JavaScript** with no server-side dependencies
- **HTML5 Canvas** for PDF display
- **Blob API** for file handling

## License

This tool is provided as-is for label imposition workflows. Ensure you have the right to process and modify any PDFs you use with this tool.