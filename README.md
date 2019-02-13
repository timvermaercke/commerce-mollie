<p align="center"><img src="./src/icon.svg" width="100" height="100" alt="Mollie for Craft Commerce icon"></p>

<h1 align="center">Mollie for Craft Commerce</h1>

This plugin provides a [Mollie](https://www.mollie.com/) integration for [Craft Commerce](https://craftcms.com/commerce).

## Requirements

This plugin requires Craft Commerce 2.0.0 or later.

## Installation

You can install this plugin from the Plugin Store or with Composer.

#### From the Plugin Store

Go to the Plugin Store in your project’s Control Panel and search for “Mollie for Craft Commerce”. Then click on the “Install” button in its modal window.

#### With Composer

Open your terminal and run the following commands:

```bash
# go to the project directory
cd /path/to/my-project.test

# tell Composer to load the plugin
composer require craftcms/commerce-mollie

# tell Craft to install the plugin
./craft install/plugin commerce-mollie
```

## Setup

To add a Mollie payment gateway, go to Commerce → Settings → Gateways, create a new gateway, and set the gateway type to “Mollie”.

### Per-Environment Configuration

Once you’ve added Mollie as a gateway in the Control Panel, you can override its settings with different values for each environment.
Mollie’s API Key settings can be set to environment variables.

First, add the following environment variable to your `.env` and `.env.example` files:

```bash
# Mollie's API Key
MOLLIE_API_KEY=""
``` 

Fill in the values in your `.env` file (leaving the values in `.env.example` blank).

Then when you use Mollie as gateway, you can reference this environment variable in the gateway settings by typing `$` followed by the environment variable name.

Only the environment variable name will be saved to your database and `project.yaml` file, not its value.
