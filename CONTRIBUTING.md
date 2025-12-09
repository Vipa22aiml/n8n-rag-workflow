# 🤝 Contributing to n8n RAG Workflow

We love your input! We want to make contributing to this project as easy and transparent as possible, whether it's:

- Reporting a bug
- Discussing the current state of the code
- Submitting a fix
- Proposing new features
- Becoming a maintainer

## 🚀 Development Process

We use GitHub to host code, to track issues and feature requests, as well as accept pull requests.

### Pull Requests
1. Fork the repo and create your branch from `main`
2. If you've added functionality, update the documentation
3. Make sure your code follows the existing style
4. Test your workflow thoroughly
5. Issue that pull request!

### Workflow Testing
Before submitting:
- Test with different file types (PDF, Excel, CSV, Text)
- Verify chat functionality works correctly
- Check that embeddings are generated properly
- Ensure database connections are stable

## 🐛 Report Bugs

**Great Bug Reports** tend to have:

- A quick summary and/or background
- Steps to reproduce
  - Be specific!
  - Give sample files if possible
- What you expected would happen
- What actually happens
- Notes (possibly including why you think this might be happening)

## 💡 Feature Requests

We're always looking for suggestions! Here are some areas where contributions would be especially welcome:

### High Priority
- [ ] Support for additional file formats (PowerPoint, Word)
- [ ] Enhanced chat UI/UX improvements
- [ ] Better error handling and logging
- [ ] Performance optimizations
- [ ] Multi-language support for documents

### Medium Priority
- [ ] Custom embedding models support
- [ ] Advanced search filters
- [ ] Document categorization
- [ ] Batch processing improvements
- [ ] API rate limiting features

### Future Ideas
- [ ] Web interface for configuration
- [ ] Docker containerization
- [ ] Cloud deployment templates
- [ ] Integration with other platforms

## 📋 Workflow Improvements

### Node Enhancements
Contributions for new nodes or improvements to existing ones:

- **File Processing**: Better extraction algorithms
- **Embedding**: Support for different embedding models
- **Chat Interface**: UI/UX improvements
- **Database**: Optimization and scaling features

### Use Case Examples
We welcome real-world examples of how you've used this workflow:

- Industry-specific implementations
- Creative use cases
- Performance benchmarks
- Integration examples

## 🛠️ Setting Up Development Environment

1. **n8n Setup**
   ```bash
   npm install -g n8n
   n8n start
   ```

2. **Database Setup**
   - Create Supabase project
   - Set up required tables
   - Configure credentials

3. **API Setup**
   - Google Cloud project with Drive and Vertex AI APIs
   - Service account credentials
   - OAuth2 setup for Drive access

4. **Testing**
   - Import the workflow template
   - Configure all credentials
   - Test with sample files

## 📝 Documentation

Help us improve our documentation:

- **README Updates**: Keep installation steps current
- **Code Comments**: Add explanations for complex logic
- **Use Case Guides**: Document real-world implementations
- **Troubleshooting**: Add solutions for common issues

## 🎨 Design Guidelines

### Workflow Design
- Keep nodes logically grouped
- Use clear, descriptive node names
- Add comments for complex operations
- Follow n8n best practices

### Documentation
- Use clear, concise language
- Include code examples where helpful
- Add screenshots for complex setups
- Keep formatting consistent

## 📞 Getting Help

- **GitHub Issues**: For bugs and feature requests
- **Discussions**: For questions and community chat
- **n8n Community**: For n8n-specific questions

## 🏷️ Labels

We use labels to categorize issues and PRs:

- `bug`: Something isn't working
- `enhancement`: New feature or request
- `documentation`: Improvements or additions to documentation
- `good first issue`: Good for newcomers
- `help wanted`: Extra attention is needed
- `question`: Further information is requested

## ⚖️ License

By contributing, you agree that your contributions will be licensed under the MIT License.

---

**Thank you for making this project better! 🙏**