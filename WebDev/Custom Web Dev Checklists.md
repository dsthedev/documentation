## Custom Web Dev Checklists

These checklists are designed to improve quality control and best practices.  They are comprehensive and repetitive on purpose.

## Environment Setup

- [ ] Visual Studio Code
  - [ ] @todo: List of extensions
- [ ] MAMP
  - [ ] @todo: Tweaks
- [ ] Browsers
  - [ ] @todo: List of browsers and desired purpose
- [ ] Node.JS & npm
  - [ ] @todo: For Foundation and Theme development
- [ ] Composer
  - [ ] @todo: For Kint PHP Debugging

## Build Process

Website's should be built locally, tested in a remote staging environment, and migrated to a production server.  Local -> Staging -> Live.  Each environment should be synced so updates can be pushed easily.

### Development

- Users
  - [ ] admin removed
  - [ ] Main Developer (Administrator)
  - [ ] Main Content Editor (Editor)
  - [ ] Client Master (Administrator)
  - [ ] Client Editor (Editor)
  - [ ] Additional Users if requested
  - [ ] Credentials stored in `.config/`
- Plugins
  - Global (**Required**)
    - [ ] ACF Pro
    - [ ] ACF: Better Search
    - [ ] Duplicator
    - [ ] Enhanced Media Library
    - [ ] EWWW Image Optimizer
    - [ ] Gravity Forms
    - [ ] iThemes Security
    - [ ] Yoast SEO
    - [ ] TinyMCE Advanced
    - [ ] WP Sync DB
    - [ ] WP Sync DB Media Files
    - [ ] WP-Optimize
    - [ ] Query Monitor
  - Optional (**Recommended**)
    - [ ] User Switching
    - [ ] WP Crontrol
    - [ ] Rewrite Rules Inspector
    - [ ] Display All Image Sizes
  - Development
    - [ ] Airplane Mode
    - [ ] Developer Loggers for Simple History
    - [ ] Kint PHP Debugger
    - [ ] Simple History
    - [ ] Transients Manager

### Staging

- [ ] Users should match Development
- [ ] Plugins - Remove all Development plugins except for Query Monitor

### Production

- [ ] Users should match Development