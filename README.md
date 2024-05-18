# My Hugo Presentation Website

This is a Hugo based website designed to showcase my personal and professional presentation. This README provides instructions on how to set up, configure and run the website.

## Table of Contents

- Features
- Requirements
- Installation
- Configuration
- Running the Website
- Deployment
- Contributing
- License

## Features

- Responsive design
- Multilingual support (English, Spanish, Portuguese)
- Customizable homepage
- Integrated social media icons
- Easy content management with Markdown

## Requirements

- Hugo (version 0.55.0 or higher)
- Git (optional, for cloning the repository)

## Installation

### Clone the Repository

```bash

git clone https://github.com/leandrocunha526/leandrocunha-website.git
cd leandrocunha-website

```

## Install Hugo

If you haven't installed Hugo yet, follow the instructions on the Hugo installation guide.

## Install the theme

The website uses the "introduction" theme. Ensure it's installed in your themes directory:

```bash

git submodule update --init --recursive
```

## Configuration

Edit the config.toml file to configure your website's settings. Below is a brief overview of the key configuration options:

### Basic Configuration

```toml

baseURL = "http://example.com/"
theme = "introduction"
DefaultContentLanguage = "en"
```

### Params

```toml

[params]
    themeStyle = "auto"
    favicon = "/img/fav.ico"
    showMenu = true
    email = "youremail@email.com"
    [params.home]
        introHeight = "fullheight"
        showLatest = true
        numberOfProjectsToShow = 3
        localTime = true
        timeZone = "America/Los_Angeles"
```

### Social Links

```toml

[[params.social]]
    url = "https://twitter.com/"
    icon = "twitter"
    icon_pack = "fab"

[[params.social]]
    url = "https://facebook.com/"
    icon = "facebook-f"
    icon_pack = "fab"

[[params.social]]
    url = "https://linkedin.com/"
    icon = "linkedin-in"
    icon_pack = "fab"
```

### Menu

```toml

[[menu.main]]
    name = "Home"
    url = "/"
    weight = 2

[[menu.main]]
    name = "Sobre"
    url = "/about/"
    weight = 3
```

## Languages

```toml

[languages]
    [languages.en]
        languageName = "English"
        languageCode = "en-us"
        contentDir = "content/en"
        title = "Introduction"

    [languages.es]
        languageName = "Español"
        languageCode = "es"
        contentDir = "content/es"
        title = "Introducción"

    [languages.de]
        languageName = "Deutsch"
        languageCode = "de"
        contentDir = "content/de"
        title = "Vorstellung"
```

## Running the Website

To run the website locally, use the Hugo server command:

```bash

hugo server -D

```

This will start a local server, and you can view your website by navigating to <http://localhost:1313> in your web browser.

## Deployment

For deployment, you can build the static files using:

```bash
hugo
```

The generated static files will be in the public/ directory, which you can then upload to your web hosting provider.

## Contributing

If you would like to contribute to this project, please fork the repository and submit a pull request. For major changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the Apache License 2.0. See the [LICENSE](LICENSE.md) file for details.
