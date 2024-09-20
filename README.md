# Template for R Projects (Following "R Package" Structure)

This template is designed to help you start a new R project by following the **R packages** structure. It is built using the `devtools` R package, which simplifies package development. `devtools` can be used via the command line or integrated into IDEs like RStudio.

## How to Create a New Project

### Option 1: From This Template

1. Clone this repository to your local machine.
2. Delete the `.git` folder to reset version control.
3. Choose the appropriate license (if available in the `licenses` folder).
4. Remove unnecessary files or folders (e.g., `licenses`, `docs`, etc.).
5. Edit this README or create a new R Markdown file for documentation.

### Option 2: Using `devtools` Command-Line

#### Install `devtools` in R

You may need to install some dependencies first.
```R
install.packages("devtools")
```

#### Create a New Package with `devtools`
1. Load `devtools` (required every time R restarts during development):
   ```R
   library(devtools)
   ```

2. Create a package directory structure:
   ```R
   create_package("path/to/package")
   ```

3. Initialize a Git repository and set up `.gitignore`:
   ```R
   use_git()
   ```

#### Add Your First R Script

1. Create a new R script in the `R/` directory:
   ```R
   use_r("filename")
   ```

2. Once you’ve added a function, load it into your environment:
   ```R
   load_all()  # Makes your functions available for testing.
   ```

#### Document Your Functions

To generate documentation for your functions:
```R
document()  # Generates .Rd files for your functions.
```

## Versioning and Tagging

Follow semantic versioning: **X.Y.Z**  
- **X**: Major release, may not be backward compatible.
- **Y**: New features, backward compatible within the same major version.
- **Z**: Minor changes or bug fixes.

## Git Branching Strategy

- **`/main` (mandatory)**: The most stable version, never breaks.
- **`/features/` (recommended)**: Develop new features (e.g., `/features/new_plot`).
- **`/releases/` (mandatory)**: For tagging releases (e.g., `/releases/rel-1-2-4`).
- **`/bugfixes/` (recommended)**: Bug fixes (can be local if simple).
- **`/clients/` (optional)**: For client-specific branches (e.g., `/clients/Novartis/projectABC`).

## Helpful Resources

- [Devtools Documentation](https://devtools.r-lib.org/index.html)  
  Official documentation for `devtools`, the package used for developing R packages.

- [R Packages Book](https://r-pkgs.org/)  
  A comprehensive guide to organizing and developing R packages.
