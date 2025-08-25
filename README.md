# CODYSSEY

Codyssey is an AI-enhanced web platform that guides students and developers on their journey to writing cleaner, more maintainable Java code. Unlike traditional online compilers or heavy enterprise tools like SonarQube, Codyssey is built with a learning-first approach, making it ideal for academic use in courses such as Advanced Programming Practice (APP) as well as for self-learners.

## Overview

At its core, Codyssey enables users to paste or upload Java code, which is then analyzed through a blend of static analysis and AI-driven mentoring. The static analysis module (leveraging tools like PMD and Checkstyle) detects common issues such as inconsistent naming, unused variables, overly complex methods, and violations of object-oriented principles. Based on these findings, the system generates a Code Quality Index (0–100), providing a clear, quantifiable measure of code health.

What sets Codyssey apart is its AI Mentor layer, which not only highlights issues but also delivers actionable improvement suggestions in simple, student-friendly language. For example, it may recommend breaking large methods into smaller ones, renaming variables for clarity, or reducing duplicate code through inheritance and interfaces. This ensures that users not only identify weaknesses but also learn how to improve their coding practices.

With an intuitive web interface, built-in code editor, detailed feedback display, and progress tracking, Codyssey transforms code review into an engaging learning experience. Faculty dashboards can also track class-wide performance, making it a valuable tool for both teaching and skill development.

## Project Structure

The project is organized into the following components:

- `/frontend` - React/TypeScript web application with Monaco Editor
- `/backend` - Spring Boot (Java 21) REST API and static analysis
- `/ai-service` - Python FastAPI service for AI mentor functionality
- `/docs` - Documentation, API contracts, and design decisions

## Key Features

- **Code Analysis** - Upload or paste Java code for instant quality feedback
- **Code Quality Index (CQI)** - Comprehensive 0-100 score with detailed breakdown
- **Issue Detection** - Static analysis finding style issues, bugs, and code smells
- **AI Mentor** - Plain-English suggestions for code improvement
- **Faculty Dashboard** - Track class progress and common issues

## Getting Started

### Prerequisites

- Frontend: Node.js and npm
- Backend: Java 21, Maven/Gradle
- AI Service: Python 3.10+, FastAPI

### Setup Instructions

*Detailed setup instructions will be added as components are developed*

## Team Collaboration

This project is being developed by a team of three, with responsibilities roughly divided as:

- Frontend development
- Backend API and static analysis
- AI/ML mentor service

Team members coordinate via Discord and GitHub issues.
