# Automatic Catalog Generator (Excel) - Documentation

## Overview

This is a browser-based catalog generator that creates printable product catalogs from Excel data and images. It automatically arranges products on A4-sized pages with customizable headers, footers, and backgrounds.

## Features

- **Excel Data Import**: Upload product information via Excel files
- **Image Management**: Associate product images by SKU filename matching
- **Automatic Layout**: Smart arrangement of 1-9 products per A4 page
- **Customization Options**: 
  - Add promotional headers with dates
  - Upload custom logos and backgrounds
  - Include footer information
- **Responsive Design**: Adapts to different numbers of products per page
- **Print-Ready Output**: Generate PDFs or print directly from browser

## Usage Guide

### Step 1: Upload Product Data
1. Prepare an Excel file with product information
2. Required columns: `page`, `sku`, `name`, `size`, `brand`, `origin`, `price`, `bbd`, `unit`, `remark`
3. Use the "page" column to specify which page each product should appear on
4. Click "Choose File" under "Step 1" to upload your Excel file

### Step 2: Upload Product Images
1. Prepare images with filenames matching product SKUs (e.g., "2327.jpg" for SKU 2327)
2. Recommended image size: 800x800 pixels
3. Maximum file size: 2MB per image
4. Click "Choose Files" under "Step 2" to upload your images

### Step 3: Customize Settings
1. Enter a promotion date/time in the text field
2. Optionally upload custom header logo, background image, and footer logo
3. The system will automatically adjust layout based on number of products per page

### Generate Catalog
1. After uploading data, the preview will automatically generate
2. Check for any missing images or data issues in the status panel
3. Click "Print / Save as PDF" to generate your final catalog

## Technical Details

### Layout System
- Supports 1-9 products per page with optimized layouts
- Automatically adjusts spacing and sizing based on product count
- Uses CSS Flexbox for responsive product arrangement
- Implements break-inside: avoid to prevent content splitting across pages

### Styling Features
- Responsive font sizing for product names and prices
- Price tags with rotation effect and gold text on red background
- Product cards with semi-transparent backgrounds and blur effects
- Support for product remarks, BBD (Best Before Date), and origin labels

### Browser Compatibility
- Requires modern browser with JavaScript enabled
- Uses File API, Canvas API, and modern CSS features
- Compatible with latest versions of Chrome, Firefox, Safari, and Edge

## File Format Specifications

### Excel Template Columns
| Column | Description | Example |
|--------|-------------|---------|
| page | Page number for product placement | 1, 2, 3 |
| sku | Product identifier | 2327 |
| name | Product name | Coconut Milk |
| size | Product size specification | 6x2900ml |
| brand | Product brand | Aroy-D |
| origin | Country of origin | Thailand |
| price | Product price | 83.90 |
| bbd | Best before date | 2026-12-31 |
| unit | Price unit | st |
| remark | Special notes | Hot Sale |

### Image Requirements
- Format: JPG, PNG, or GIF
- Recommended size: 800x800 pixels
- Maximum size: 2MB
- Filename must match SKU exactly (e.g., "2327.jpg" for SKU 2327)

## Troubleshooting

### Common Issues
1. **Missing Images**: Ensure filenames exactly match SKUs (case-sensitive)
2. **Layout Problems**: Check that Excel data is properly formatted
3. **Performance Issues**: Reduce image sizes or number of products per page
4. **Print Problems**: Use Chrome's Save as PDF option for best results

### Error Messages
- "Excel parsing failed": Check Excel file format and structure
- "Image compression failed": Try reducing image file size
- "Layout warnings": Some content may not fit properly on page

## Customization Options

### Header Customization
- Upload custom company logo (recommended size: 400x100px)
- Modify promotional text and dates
- Add background images (recommended size: 1240x1754px)

### Footer Customization
- Add custom footer logo (recommended size: 100x100px)
- Modify company contact information
- Update legal text and terms

## Print Settings

For best print results:
1. Use Chrome browser
2. Select "Save as PDF" in the print dialog
3. Set margins to "None" or "Minimum"
4. Ensure "Background graphics" is enabled in print options
5. Paper size: A4

The system automatically generates properly sized A4 pages with 10mm margins and handles page breaks appropriately.
