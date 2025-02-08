# Eigensite

### Jekyll Dynamic Resource Blog
This project is a Jekyll-based website that dynamically generates pages for resource blogs with unique URLs based on an `order` parameter. It includes features like collections, custom permalinks, and dynamic routing for improved content management.

### Features

- **Dynamic URL Structure**: Each blog post is accessible via a URL structured as `/page/order/1/`.
- **Collections**: Resources are organized in a `resources_blog` collection for easy management.
- **Customizable Layouts**: Supports flexible layouts and components for dynamic pages.
- **Liquid Templates**: Uses Jekyll's Liquid syntax for dynamic content rendering.
- **Responsive Design**: Fully responsive and optimized for different devices.

## Getting Started

**Prerequisites**

- Ruby (latest version)
- Jekyll (latest version)

**Installation**

1. Clone the repository:

``` terminal
git clone https://github.com/eigenspacedesign/eigensite.git
```

  

1. Navigate to the project directory:
```
cd eigensite
```

1. Install dependencies:

```
bundle install
```

  

**Development Server**

To start the development server:

```
jekyll serve
```

or

```
bundle exec jekyll serve
```

**Access the Site on Other Devices:**

Replace `192.168.29.105` with the actual local IP of your machine:

```
bundle exec jekyll serve --host 192.168.29.105 --watch
```

Visit http://localhost:4000 or http://192.168.29.105:4000 to see the site.

  

**Build for Production**

To build the site for production:

```
jekyll build
```

  

**Debugging**

Run the following command for detailed error output:

```
jekyll build --trace
```

  

**Gem**
gem build eigensite.gemspec
gem install eigensite-0.1.0.gem


