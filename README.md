# Home Assistant Blueprints Collection

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Home Assistant](https://img.shields.io/badge/Home%20Assistant-supported-blue.svg)](https://www.home-assistant.io/)
[![GitHub stars](https://img.shields.io/github/stars/Dzhuneyt/home-assistant-blueprints.svg)](https://github.com/Dzhuneyt/home-assistant-blueprints/stargazers)

A curated collection of automation blueprints for [Home Assistant](https://www.home-assistant.io/) to help you create smart home automations with ease.

## What are Home Assistant Blueprints?

Blueprints are a Home Assistant feature that allows you to create automations from pre-made templates. They provide a user-friendly way to set up complex automations without writing YAML code from scratch. Blueprints can be shared, imported, and customized to fit your specific needs.

## Available Blueprints

### 🌡️ AC Turn On Comfort Mode

**File:** `ac_turn_on_comfort_mode.yaml`

**Description:** Automatically switches your air conditioning to a comfort mode with your preferred temperature when a specific HVAC mode is detected. Perfect for seasonal automation - switch to heating mode in winter and cooling mode in summer.

**Features:**
- Monitor any climate entity for HVAC mode changes
- Configurable trigger mode (typically "auto")
- Set target HVAC mode (heat/cool) and temperature
- Single execution mode to prevent conflicts

**Use Cases:**
- Automatically switch from "auto" to "heat" mode at 22°C during winter
- Switch from "auto" to "cool" mode at 24°C during summer
- Ensure consistent comfort settings across different AC units

## Installation

### Method 1: Direct Import (Recommended)

1. In Home Assistant, go to **Settings** → **Automations & Scenes** → **Blueprints**
2. Click **Import Blueprint**
3. Paste the raw URL of the blueprint you want:
   ```
   https://raw.githubusercontent.com/Dzhuneyt/home-assistant-blueprints/main/blueprints/ac_turn_on_comfort_mode.yaml
   ```
4. Click **Preview Blueprint** and then **Import Blueprint**

### Method 2: Manual Download

1. Download the desired blueprint file from the [`blueprints/`](./blueprints/) directory
2. Place the file in your Home Assistant `config/blueprints/automation/` directory
3. Restart Home Assistant or reload automation blueprints

## Usage

After importing a blueprint:

1. Go to **Settings** → **Automations & Scenes** → **Automations**
2. Click **Create Automation** → **Use Blueprint**
3. Select the imported blueprint
4. Configure the required parameters:
   - **Climate Entity**: Choose your AC/climate device
   - **Trigger Mode**: Select the mode that triggers the automation
   - **Target HVAC Mode**: Choose the desired mode (heat/cool)
   - **Temperature**: Set your comfort temperature
5. Save the automation with a descriptive name

### Example Configuration

For the AC Comfort Mode blueprint:
- **Climate Entity**: `climate.living_room_ac`
- **Trigger Mode**: `auto`
- **HVAC Mode**: `cool` (for summer) or `heat` (for winter)
- **Temperature**: `24°C` (summer) or `22°C` (winter)

## Contributing

We welcome contributions! Here's how you can help:

### Adding New Blueprints

1. Fork this repository
2. Create a new blueprint file in the `blueprints/` directory
3. Follow the naming convention: `descriptive_name.yaml`
4. Include proper metadata in your blueprint:
   ```yaml
   # Author: Your Name (https://your-website.com)
   # Originally published at: https://github.com/Dzhuneyt/home-assistant-blueprints
   # License: MIT
   ```
5. Update this README with your blueprint description
6. Submit a pull request

### Blueprint Requirements

- **Clear documentation**: Include name, description, and input explanations
- **Proper selectors**: Use appropriate input selectors for user-friendly configuration
- **Error handling**: Consider edge cases and provide sensible defaults
- **Testing**: Verify your blueprint works in different scenarios
- **Originality**: Ensure your blueprint adds unique value

### Reporting Issues

Found a bug or have a suggestion? Please [open an issue](https://github.com/Dzhuneyt/home-assistant-blueprints/issues) with:
- Clear description of the problem or suggestion
- Steps to reproduce (for bugs)
- Your Home Assistant version
- Relevant configuration details

## Support

- **Documentation**: [Home Assistant Blueprints Documentation](https://www.home-assistant.io/docs/blueprint/)
- **Community**: [Home Assistant Community Forum](https://community.home-assistant.io/)
- **Issues**: [GitHub Issues](https://github.com/Dzhuneyt/home-assistant-blueprints/issues)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Author

**Dzhuneyt** - [Website](https://dzhuneyt.com) | [GitHub](https://github.com/Dzhuneyt)

---

⭐ If you find these blueprints helpful, please consider starring this repository!

## Roadmap

- [ ] Add more climate control blueprints
- [ ] Lighting automation blueprints
- [ ] Security and monitoring blueprints
- [ ] Energy management blueprints
- [ ] Seasonal automation blueprints

*Have an idea for a blueprint? [Open an issue](https://github.com/Dzhuneyt/home-assistant-blueprints/issues) and let's discuss it!*