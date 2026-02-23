# Contributing to Bangladesh VAT Calculator

First off, thank you for considering contributing to the Bangladesh VAT Calculator! 🎉

## Table of Contents
- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
- [Development Setup](#development-setup)
- [Coding Standards](#coding-standards)
- [Pull Request Process](#pull-request-process)
- [Reporting Bugs](#reporting-bugs)
- [Suggesting Enhancements](#suggesting-enhancements)

## Code of Conduct

This project and everyone participating in it is governed by our Code of Conduct. By participating, you are expected to uphold this code. Please report unacceptable behavior to the project maintainers.

### Our Pledge
- Be respectful and inclusive
- Be patient and welcoming
- Be considerate and constructive
- Focus on what is best for the community

## How Can I Contribute?

### 🐛 Reporting Bugs

Before creating bug reports, please check the existing issues to avoid duplicates.

**To submit a good bug report:**
1. Use a clear and descriptive title
2. Describe the exact steps to reproduce the problem
3. Provide specific examples
4. Describe the behavior you observed and what you expected
5. Include screenshots if possible
6. Include browser and OS information

**Example Bug Report:**
```markdown
**Title:** VAT calculation incorrect for 7.5% rate

**Description:**
When calculating VAT with 7.5% rate, the result shows incorrect value.

**Steps to Reproduce:**
1. Select "Add VAT to Price"
2. Enter ৳10000
3. Select 7.5% VAT rate
4. Click Calculate

**Expected Result:**
VAT Amount: ৳750.00

**Actual Result:**
VAT Amount: ৳700.00

**Browser:** Chrome 120
**OS:** Windows 11
```

### 💡 Suggesting Enhancements

Enhancement suggestions are welcome! Please include:
- Clear and descriptive title
- Detailed description of the proposed feature
- Explain why this enhancement would be useful
- List any alternatives you've considered
- Include mockups or examples if applicable

**Example Enhancement Suggestion:**
```markdown
**Title:** Add Dark Mode Toggle

**Description:**
Add a dark/light mode toggle button to allow users to switch between themes.

**Benefits:**
- Better viewing experience in low-light conditions
- Reduces eye strain
- Modern user preference

**Implementation Ideas:**
- Toggle button in header
- Store preference in localStorage
- Smooth transition between modes
```

### 🔧 Code Contributions

We welcome code contributions! Here are some areas where you can help:

**Priority Features:**
- [ ] Print functionality
- [ ] Export to PDF
- [ ] Calculation history
- [ ] Dark mode
- [ ] PWA support
- [ ] Offline capability

**Improvements:**
- [ ] Performance optimization
- [ ] Accessibility enhancements
- [ ] Mobile UX improvements
- [ ] Additional language support
- [ ] Code documentation

## Development Setup

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, Edge)
- A text editor (VS Code, Sublime Text, etc.)
- Git for version control

### Getting Started

1. **Fork the repository**
   ```bash
   # Click the "Fork" button on GitHub
   ```

2. **Clone your fork**
   ```bash
   git clone https://github.com/YOUR-USERNAME/bangladesh-vat-calculator.git
   cd bangladesh-vat-calculator
   ```

3. **Create a branch**
   ```bash
   git checkout -b feature/your-feature-name
   # or
   git checkout -b fix/your-bug-fix
   ```

4. **Make your changes**
   - Edit `index.html`
   - Test in multiple browsers
   - Ensure responsive design works

5. **Test your changes**
   - Open `index.html` in browsers
   - Test all calculation modes
   - Verify mobile responsiveness
   - Check console for errors

6. **Commit your changes**
   ```bash
   git add .
   git commit -m "Add: Brief description of your changes"
   ```

7. **Push to your fork**
   ```bash
   git push origin feature/your-feature-name
   ```

8. **Open a Pull Request**
   - Go to the original repository
   - Click "New Pull Request"
   - Select your branch
   - Fill in the PR template

## Coding Standards

### HTML
- Use semantic HTML5 elements
- Maintain proper indentation (2 spaces)
- Add comments for complex sections
- Ensure accessibility (ARIA labels, alt text)

### CSS
- Follow existing style patterns
- Use Tailwind CSS utility classes
- Add custom CSS in `<style>` section
- Maintain mobile-first approach

### JavaScript
- Use ES6+ syntax
- Write clear, descriptive function names
- Add JSDoc comments for functions
- Use `const` and `let` (avoid `var`)
- Handle errors gracefully
- Validate all user inputs

### Example Function Documentation
```javascript
/**
 * Calculate VAT amount from base price
 * @param {number} basePrice - The base price before VAT
 * @param {number} vatRate - VAT percentage rate
 * @returns {number} VAT amount
 */
function calculateVATAmount(basePrice, vatRate) {
    return basePrice * (vatRate / 100);
}
```

### Code Style
```javascript
// Good
function addVAT(basePrice, vatRate) {
    const vatAmount = basePrice * (vatRate / 100);
    const totalPrice = basePrice + vatAmount;
    return { vatAmount, totalPrice };
}

// Avoid
function add_vat(bp,vr){
    var va=bp*(vr/100);
    return bp+va;
}
```

## Pull Request Process

### Before Submitting
- [ ] Test in Chrome, Firefox, and Safari
- [ ] Test on mobile devices
- [ ] Check for console errors
- [ ] Verify all calculations are accurate
- [ ] Update README if needed
- [ ] Add comments to your code

### PR Template
```markdown
## Description
Brief description of changes

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Enhancement
- [ ] Documentation update

## Testing Done
- [ ] Tested in Chrome
- [ ] Tested in Firefox
- [ ] Tested in Safari
- [ ] Tested on mobile
- [ ] All calculations verified

## Screenshots (if applicable)
Add screenshots here

## Checklist
- [ ] Code follows project style guidelines
- [ ] Self-review completed
- [ ] Comments added where needed
- [ ] No console errors
- [ ] Works on mobile devices
```

### Review Process
1. Maintainer reviews your PR
2. Feedback may be provided
3. Make requested changes
4. PR is approved and merged

## Testing Guidelines

### Manual Testing Checklist
- [ ] **Add VAT Mode**
  - [ ] Enter ৳10000, 15% → Should show ৳1500 VAT, ৳11500 total
  - [ ] Test with decimal values
  - [ ] Test with zero
  - [ ] Test with very large numbers

- [ ] **Remove VAT Mode**
  - [ ] Enter ৳11500, 15% → Should show ৳10000 base, ৳1500 VAT
  - [ ] Verify formula accuracy

- [ ] **VAT Amount Only Mode**
  - [ ] Enter ৳10000, 15% → Should show ৳1500 VAT

- [ ] **Input Validation**
  - [ ] Empty fields show error
  - [ ] Negative numbers rejected
  - [ ] Zero handled correctly
  - [ ] Invalid characters rejected

- [ ] **UI/UX**
  - [ ] All buttons work
  - [ ] Quick VAT buttons update field
  - [ ] Reset clears all fields
  - [ ] Results display correctly
  - [ ] Animations smooth

- [ ] **Responsive Design**
  - [ ] Works on mobile (320px+)
  - [ ] Works on tablet (768px+)
  - [ ] Works on desktop (1024px+)

## Bangladesh VAT Compliance

When contributing calculations or tax-related features:
- Verify against VAT Act 2012
- Check NBR guidelines
- Ensure accuracy for all rates (5%, 7.5%, 15%)
- Add appropriate disclaimers
- Cite official sources when possible

## Documentation

When adding features:
- Update README.md
- Add inline code comments
- Update usage examples if needed
- Document new functions

## Questions?

Feel free to:
- Open an issue for discussion
- Ask in pull request comments
- Contact maintainers

## Recognition

Contributors will be recognized in:
- README.md Contributors section
- GitHub contributors page
- Release notes

## License

By contributing, you agree that your contributions will be licensed under the MIT License.

---

Thank you for contributing to making VAT calculations easier for Bangladesh! 🇧🇩 🎉
