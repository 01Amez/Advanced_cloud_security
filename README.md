# Cloud Security Comparison Platform

A comprehensive Next.js web application that demonstrates and compares **Agent-Based** vs **Agentless** cloud security tools through realistic security scanning simulations.

![Cloud Security Comparison](https://img.shields.io/badge/Next.js-14.2.3-black?style=for-the-badge&logo=next.js)
![License](https://img.shields.io/badge/license-MIT-blue?style=for-the-badge)

## 🎯 Overview

This application simulates a realistic multi-service cloud environment (AWS/Azure/GCP-like) with intentional security vulnerabilities and demonstrates how two different security scanning approaches detect and report these issues:

- **Agent-Based Security Tool**: Deep inspection with installed agents on each resource
- **Agentless Security Tool**: API-based scanning without agent installation

## ✨ Features

### 🖥️ Interactive Windows Cloud Preview Environment**
- **Real-time File System Monitoring**: Create files and folders in a simulated Windows environment
- **Instant Security Detection**: All file/folder changes are automatically tracked and analyzed
- **Agentbased Integration**: Created items appear in real-time in the Agentless Security Findings
- **Detailed Security Analysis**: Click any detected file/folder to view:
  - CVSS scores and risk assessments
  - Compliance mapping (SOC2, ISO 27001, NIST, PCI-DSS, GDPR)
  - 8 actionable remediation steps
  - Full change history with timestamps
- **Interactive Desktop**: Complete Windows-like environment with:
  - File Explorer for navigating directories
  - Desktop icons (This PC, Recycle Bin, Documents, Downloads)
  - Right-click context menus for creating files/folders
  - Notepad for viewing and editing text files
  - Taskbar with Start menu and running applications


## 🛠️ Technology Stack

- **Frontend**: Next.js 14.2.3, React 18
- **UI Components**: shadcn/ui, Tailwind CSS
- **Backend**: Next.js API Routes
- **Database**: MongoDB (for potential extensions)
- **Icons**: Lucide React
- **Styling**: Tailwind CSS with custom design system

## 🖥️ Windows Cloud Preview - Detailed Guide

The Windows Cloud Preview is an interactive environment that simulates a Windows operating system for security testing purposes.

### Features

#### 🎯 Real-time File System Monitoring
Every file or folder you create is automatically:
- **Tracked**: Change type, name, path, and timestamp recorded
- **Analyzed**: Security impact assessment performed
- **Reported**: Appears in Agentless Security Findings
- **Detailed**: Click for comprehensive security analysis

#### 🗂️ File System Operations
- **Create Files**: Right-click → New → Text Document
- **Create Folders**: Right-click → New → Folder
- **Navigate**: Use File Explorer to browse directories
- **Edit Files**: Double-click text files to open in Notepad
- **Desktop Icons**: Quick access to common locations

### How It Works

1. **User Action**: Create/delete/modify file or folder in Windows environment
2. **Detection**: Change is captured with full metadata
3. **Transmission**: Change data sent to scanning system
4. **Analysis**: Agent-based scanner evaluates security implications
5. **Reporting**: Finding appears in Agent-based Security Findings
6. **Detail View**: Click to see comprehensive analysis

## 📦 Installation

### Prerequisites
- Node.js 18+ or Yarn
- MongoDB (optional, for extensions)

### Setup

1. **Clone the repository**
```bash
git clone <repository-url>
cd Advanced-cloud-security
```

2. **Install dependencies**
```bash
yarn install
```

3. **Environment Variables**
Create a `.env` file in the root directory:
```env
MONGO_URL=mongodb://localhost:27017/Advanced-cloud-security
NEXT_PUBLIC_BASE_URL=http://localhost:3000
```

4. **Run the development server**
```bash
yarn dev
```

5. **Open in browser**
Navigate to [http://localhost:3000](http://localhost:3000)

## 🏗️ Project Structure

```
/app
├── app/
│   ├── api/
│   │   └── [[...path]]/
│   │       └── route.js          # Backend API routes
│   ├── page.js                   # Main application page
│   ├── layout.js                 # Root layout
│   └── globals.css              # Global styles
├── components/
│   └── ui/                       # shadcn/ui components
├── lib/
│   └── utils/                    # Utility functions
├── public/                       # Static assets
├── .env                          # Environment variables
├── package.json                  # Dependencies
├── tailwind.config.js           # Tailwind configuration
└── README.md                     # This file
```
