# Contributing to Productivity & Project Governance Platform

## Development Workflow

This project follows a structured virtual team approach with AI agents handling different phases:

### Pipeline Stages
1. **BA_INTERVIEW** - Requirements gathering (8 questions)
2. **BA_UNDERSTANDING_REVIEW** - Understanding summary approval ✅
3. **BA_BRD_WORKING/REVIEW** - Business Requirements Document 🔄
4. **BA_FSD_WORKING/REVIEW** - Functional Specification Document
5. **ARCHITECT_SOW_WORKING/REVIEW** - Statement of Work
6. **ARCHITECT_DESIGN_WORKING/REVIEW** - Technical Architecture
7. **DEV_WORKING** - Implementation
8. **TEST_CYCLE** - Quality Assurance
9. **DELIVERY_REVIEW** - Final approval
10. **DONE** - Project complete

## Document Standards

### Business Analyst Documents
- **Understanding Summary**: Strategic overview and deep technical analysis
- **BRD**: Comprehensive requirements with MoSCoW prioritization, user stories, ROI analysis
- **FSD**: Detailed functional specifications with Given/When/Then acceptance criteria

### Architect Documents
- **Statement of Work**: Module breakdown and effort estimates
- **Tech Stack**: Technology choices with justification
- **Architecture**: System design and scalability planning
- **Data Models**: Complete Sequelize ORM schemas
- **API Specification**: Every endpoint with request/response schemas
- **Dev Handoff**: Module specifications for development

## Code Standards (When Development Begins)

### Technology Requirements
- **Next.js 14+** with App Router
- **TypeScript 5+** (no `any` types allowed)
- **PostgreSQL 15+** with Sequelize ORM 6+
- **Tailwind CSS** for styling
- **Zod** for all input validation

### Security Requirements
- All inputs validated with Zod schemas
- Parameterized queries only (no string concatenation)
- No hardcoded secrets or credentials
- Proper error handling and logging
- RBAC implementation for all endpoints

### Quality Standards
- Test coverage >90%
- TypeScript strict mode enabled
- ESLint and Prettier configuration
- Automated security scanning
- Performance monitoring

## Review Process

### Approval Gates
Each `_REVIEW` stage requires explicit user approval:
- `/approve` - Advance to next stage
- `/reject [feedback]` - Revise with provided feedback

### Quality Checklist
- [ ] All requirements traceable to business objectives
- [ ] Security considerations addressed
- [ ] Performance requirements specified
- [ ] User experience validated
- [ ] Integration points defined
- [ ] Test coverage planned
- [ ] Deployment strategy outlined

## Project Structure

```
📁 Project Root/
├── 📄 README.md - Project overview
├── 📄 CONTRIBUTING.md - This file
├── 📄 project.json - Project state and metadata
├── 📁 ba/ - Business Analyst deliverables
├── 📁 architect/ - Solution Architect deliverables
├── 📁 developer/ - Development deliverables
└── 📁 tester/ - Quality Assurance deliverables
```

## Getting Started

1. Review the current project status in `project.json`
2. Read the approved documents in order:
   - Understanding Summary (context)
   - BRD (requirements) 
   - FSD (specifications)
3. Follow the virtual team pipeline process
4. Ensure all approval gates are satisfied before advancement

## Contact

This project is managed by a virtual development team with AI agents. All communication flows through the orchestration system with proper stage management and approval workflows.