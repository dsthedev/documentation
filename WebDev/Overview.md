# Custom Website Process

This document will cover the process, requirements, and recommendations for creating a custom website.  It will use WordPress as a platform, however most other tools should be able to follow along.  Since I'm mostly a developer, the content and design sections will not be as thorough as the development sections.

Eventually this will be split into individual documents, then linked together as a reference site hosted somewhere for public access.

## Hosting

* Hosting environment
  * WordPress?
    * PHP 7 (5.6 supported)
    * MySQL
  * SSL ([Let's Encrypt](https://letsencrypt.org/))
    * List of hosts that support Lets Encrypt [here](https://community.letsencrypt.org/t/web-hosting-who-support-lets-encrypt/6920)
  * [Cloudflare](https://www.cloudflare.com/)
  * Recommended Hosts
    * [Siteground](https://www.siteground.com/), [Geekghost](http://geekghost.net/), more to come
* Developer access





## Content

* "Content is King"
  * The whole point of a website is to host some kind of content
  * It could be text, images, products, etc
* Sitemap
  * How will the content be organized?
  * Start with most important and branch out
  * Should go from "easiest to digest" and progress to most technical details
* SEO - Should be search engine optimized
* Analyze feature requirements
  * Image galleries, product catalogs, case studies, etc
* API's & integrations
  * Google Maps, YouTube, Github, etc





## Design

* Wireframes

  * Outlines each pages layout with components
  * Notes on interaction and flow (links to other pages)
  * Show alternate states for menus, cta's, sliders, buttons, etc
  * Light notes about technical details are okay (animation/interaction)

* Aesthetic Concept

  * What will the look and feel of the website or collateral be?
  * Typography, colors, textures, imagery

* Design Drafts

  - Mobile First
    - Start with bare essentials that will fit on a small screen
    - Add extra content and design elements as the size increases

  * First draft of each page
  * Get feedback from partners, clients, work associates, etc
  * Implement change as necessary

* Final Design

  * Flatten, optimize, and host final designs somewhere





## Development

* Setup Environments
  * Localhost
    * Create database and credentials
    * Add to project access document
  * Staging
  * DB / File Sync

### Build Stages (WordPress)

#### Alpha (Setup) 0.0.1

* Deploy new installation of WordPress
* Add debugging tools
* Create templates for each unique view
  * Front page, portfolio archives, product page, etc
* Create components
  * Add new field group for each with necessary fields
  * Create partial file with markup, inject field groups
  * Create empty SCSS files for each, add imports to main stylesheet
* Backup & Sync to staging environment review 0.0.9

#### Beta (Style) 0.1.0

* Add fonts & colors
* Configure SCSS settings
* Add spacing and light styling to each component
  * Headers, font changes, alignment, background & border colors, etc
* Backup & Sync to staging environment for review 0.9.0

#### Charlie (Finalize) 1.0.0

* Animations
* Reveals
* Fine tuning styles
* Backup & Sync to staging environment for review 1.9.0

#### Delta (Deploy) 2.0.0

* ​

## Deployment

* ​

###### TBC...
