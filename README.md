# SRT Exporter

An Electron application with React, Vite, and Ant Design for exporting SRT files from CapCut and Jianying projects.

## Demo

![SRT Exporter Demo](./assets/demot_0.png)

## Features

- 🔍 **Browse CapCut/Jianying Drafts**: Auto-discover and display all CapCut and Jianying projects
- 📝 **Single SRT Export**: Select a project and export SRT file
- 🚀 **Batch Export**: Select multiple projects and export all at once
- 📋 **Copy Content**: Copy text or SRT content to clipboard
- 🔍 **Search**: Search projects by name
- 🌙 **Dark Theme**: Beautiful dark interface
- 💾 **Save Settings**: Auto-save directory paths
- ℹ️ **About Page**: Author info, repository and support
- 🔗 **Quick Links**: Access GitHub, report bugs, request features
- 🎯 **Version Support**: Compatible with CapCut v5.x and v6.x

## Installation

### System Requirements
- Node.js 16+
- npm or yarn

### Install Dependencies

```bash
npm install
```

### Run Application in Development Mode

```bash
npm run electron:dev
```

### Build Application

```bash
# Build for all platforms
npm run dist

# Build for Windows
npm run dist:win

# Build for macOS
npm run dist:mac
```

## Usage

### 1. Select CapCut/Jianying Drafts Directory
- Click "Browse" button to select CapCut Drafts directory
- Usually located at: `C:\Users\<YourUsername>\AppData\Local\CapCut Drafts`
- Or Jianying Drafts directory: `C:\Users\<YourUsername>\AppData\Local\JianyingPro\User Data\Projects\com.lveditor.draft`
- Click "Load" to load project list

### 2. Single SRT Export
- Click on a project in the list
- Click "Extract SRT" to extract subtitle content
- Click "Save SRT File" to save the file

### 3. Batch Export
- Select output directory using "Browse Output"
- Check the checkboxes of projects you want to export
- Click "Batch Export SRT Files"

### 4. Other Features
- **Search**: Type project name to search
- **Copy Text**: Copy plain text content
- **Copy SRT**: Copy SRT format content
- **Select All/Deselect All**: Select/deselect all projects
- **About Page**: Click "About" in sidebar to view detailed information

### 5. About Page
- **Author Information**: Details about version and development team
- **Repository**: Direct link to GitHub repository
- **Bug Reports**: Create new issues for bug reports
- **Feature Requests**: Submit feature requests
- **Technical Information**: Details about technologies used
- **System Requirements**: Compatible with Windows, macOS, Linux

## Project Structure

```
srt-exporter/
├── electron/
│   ├── main.js          # Electron main process
│   └── preload.js       # Preload script
├── src/
│   ├── App.jsx          # React main component
│   ├── main.jsx         # React entry point
│   └── index.css        # Dark theme styles
├── package.json
├── vite.config.js
└── README.md
```

## Technologies Used

- **Electron**: Desktop app framework
- **React**: UI library
- **Vite**: Build tool and dev server
- **Ant Design**: UI component library
- **Node.js**: Runtime environment

## CapCut/Jianying Directory Structure

The application searches for directories with this structure:

```
📁 CapCut Drafts/
├── 📁 Project1/
│   ├── 📄 draft_content.json  # File containing subtitle data
│   └── 📄 draft_cover.jpg     # Thumbnail (optional)
└── 📁 Project2/
    ├── 📄 draft_content.json
    └── 📄 draft_cover.jpg

📁 JianyingPro\User Data\Projects\com.lveditor.draft (剪映)
├── 📁 项目1/
│   ├── 📄 draft_content.json
│   └── 📄 draft_cover.jpg
└── 📁 项目2/
    ├── 📄 draft_content.json
    └── 📄 draft_cover.jpg
```

## Troubleshooting

### No Projects Found
- Check the CapCut/Jianying Drafts directory path
- Ensure project directories contain `draft_content.json` files

### Error When Exporting SRT
- Check if the project contains subtitle tracks
- Ensure `draft_content.json` file is not corrupted

### Application Won't Start
- Check Node.js version (requires 16+)
- Run `npm install` to reinstall dependencies

## License

MIT License
