# ChronoGlance
Home Assistant Theme that will soon Dynamically Adjust based on Events, Holidays, and Mood.

### ChronoGlance
<img width="500" alt="chronoglance-light" src="Screenshots/Dark and Default.PNG" /><img width="500" alt="chronoglance-light" src="Screenshots/Dark and Default.PNG" />
  

## Installation

1. You can install the theme with [HACS](https://hacs.xyz/docs/setup/download):

[![Open your Home Assistant instance and open a repository inside the Home Assistant Community Store.](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=DeBendeBurcht&repository=ChronoGlance&category=theme)

> [!NOTE]  
> Install the [`uix`](https://github.com/Lint-Free-Technology/uix) integration via HACS to make the sidebar transparent. It's a drop-in replacement for card-mod with backwards compatibility. After installing, don't forget to [add the integration for it](https://uix.lf.technology/quick-start/#add-ui-extension-service).

2. You should see the "ChronoGlance" themes appear in your list of themes.

If it's missing, try reloading your themes or adding the following code to your `configuration.yaml` file (reboot required):

```yaml
frontend:
  themes: !include_dir_merge_named themes
```

3. (Optional) You can set this as the default theme with the following automation:
```
alias: Frontend - Change theme
trigger:
  - platform: homeassistant
    event: start
action:
  - service: frontend.set_theme
    data:
      name: chronoglance
```
