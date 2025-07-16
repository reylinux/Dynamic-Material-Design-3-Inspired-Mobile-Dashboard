# Dynamic-Material-Design-3-Inspired-Mobile-Dashboard
**INTRODUCTION**

Welcome to my custom **Material Design 3–inspired mobile dashboard** — a project born from my passion for clean, intuitive interfaces and rich color customization.

This project is the result of my passion for crafting clean, intuitive UIs with a focus on **dynamic color customization**. Inspired by **Google's Material You** design language, the dashboard adapts accent colors across all elements — while keeping usability and clarity at the core.

Whether it's controlling lights, viewing sensor data, or managing automations, every element is designed to be **intuitive at a glance**, without sacrificing personality or flexibility.

If you love dashboards that are both **aesthetically pleasing and highly functional**, this project might inspire your next setup.

**🧱 Behind the Scenes: Theming & Code Optimization**

To enable the dynamic theming system, you'll need to set up an [input_select](https://github.com/reylinux/Dynamic-Material-Design-3-Inspired-Mobile-Dashboard/blob/main/Input%20Select.txt) helper along with a few [template sensors](https://github.com/reylinux/Dynamic-Material-Design-3-Inspired-Mobile-Dashboard/blob/main/Dynamic%20Theme%20Sensor.txt) that drive the color mapping logic. I recommend using a popup card as the interface for selecting accent colors — it keeps the dashboard clean while allowing easy interaction.

It's also worth noting that I’ve decluttered most of the repetitive card definitions using [decluttering-card](https://github.com/custom-cards/decluttering-card). This not only streamlined the configuration but also reduced over 3,000 lines of YAML, significantly improving maintainability and performance.

**📦 Required HACS Integrations & Add-ons**

Below is a list of everything you’ll need to install from HACS to achieve a 100% match of the layout and functionality shown in the showcase:

**Cards**
- [Button Card](https://github.com/custom-cards/button-card)
- [Expander Card](https://github.com/Alia5/lovelace-expander-card)
- [Mushroom](https://github.com/piitaya/lovelace-mushroom)
- [My-slilder-v2](https://github.com/AnthonMS/my-cards/blob/main/docs/cards/slider-v2.md)

**Graphs**
- [Mini Graph Card](https://github.com/kalkih/mini-graph-card)
- [Waterfall History Card](https://github.com/sxdjt/horizontal-waterfall-history-card)

**Layouts / templating:**
- [Auto Entities](https://github.com/thomasloven/lovelace-auto-entities)
- [Card-Mod](https://github.com/thomasloven/lovelace-card-mod)
- [Config Template Card](https://github.com/iantrich/config-template-card)
- [Decluttering Card](https://github.com/custom-cards/decluttering-card)
- [Layout Card](https://github.com/thomasloven/lovelace-layout-card)
- [Local Conditional Card](https://github.com/PiotrMachowski/Home-Assistant-Lovelace-Local-Conditional-card) 
- [Paper Buttons Row](https://github.com/jcwillox/lovelace-paper-buttons-row)
- [Stack in Card](https://github.com/custom-cards/stack-in-card)
- [Vertical Stack in Card](https://github.com/ofekashery/vertical-stack-in-card)

**Theme**
- [Material You Theme](https://github.com/Nerwyn/material-you-theme)

**ETC**
- [Alarmo](https://github.com/nielsfaber/alarmo)
- [Calendar Card Pro](https://github.com/alexpfau/calendar-card-pro)
- [Mini Media Player](https://github.com/kalkih/mini-media-player)
- [WebRTC Camera](https://github.com/AlexxIT/WebRTC)


Without further ado, let's dive in!

# 🌤️ Homepage: Alerts, Climate & Presence
<img width="1600" height="1440" alt="2" src="https://github.com/user-attachments/assets/263ef5b6-e7ed-404e-8817-52844e4ced22" />

The homepage includes:

- [Alarm & notification indicators](https://github.com/reylinux/Dynamic-Material-Design-3-Inspired-Mobile-Dashboard/blob/main/Alarm%20&%20Notification%20Indicators.txt)
- [Weather Forecast with Buttons](https://github.com/reylinux/Dynamic-Material-Design-3-Inspired-Mobile-Dashboard/blob/main/Weather%20Forecast%20Buttons)
- [Three-button color selector (Home, Environment, Active)](https://github.com/reylinux/Dynamic-Material-Design-3-Inspired-Mobile-Dashboard/blob/main/Three%20Buttons%20Selectors.txt)
- [Climate control section with indoor/outdoor temperature](https://github.com/reylinux/Dynamic-Material-Design-3-Inspired-Mobile-Dashboard/blob/main/Climate%20Control.txt)

  _For the outdoor weather condition icon, you will need this [template sensor](https://github.com/reylinux/Dynamic-Material-Design-3-Inspired-Mobile-Dashboard/blob/main/Weather%20Condition%20Icon%20Sensor) to get it working._
- [Room occupancy & presence sensor toggles (sliders)](https://github.com/reylinux/Dynamic-Material-Design-3-Inspired-Mobile-Dashboard/blob/main/Room%20Occupancy%20%26%20Presence%20Sensors%20Toggle)  
- A hidden calendar beneath the [navbar](https://github.com/reylinux/Dynamic-Material-Design-3-Inspired-Mobile-Dashboard/blob/main/Navbar.txt), accessible on interaction  
- [Indoor temperature](https://github.com/reylinux/Dynamic-Material-Design-3-Inspired-Mobile-Dashboard/blob/main/Indoor%20Temperature%20Card) & humidity cards shift hue based on the current reading (from violet → red).
- A dedicated "Currently Active" section shows lights, switches, fans, music, and any active automation in real-time.

If you’d like to copy the **full code for the three-button color selector** and the supporting components beneath it, you can find it [here](https://github.com/reylinux/Dynamic-Material-Design-3-Inspired-Mobile-Dashboard/blob/main/Button%20Full%20Code.txt)

# 🏠 Room Overview, Cameras & Weather Panel
<img width="3200" height="2880" alt="3" src="https://github.com/user-attachments/assets/0d03c4ec-9d95-404f-ae03-403b987572ac" />

- Each [room card](https://github.com/reylinux/Dynamic-Material-Design-3-Inspired-Mobile-Dashboard/blob/main/Room%20Card%20Example.txt) shows light toggles, climate status, and door/window sensors — with background color reflecting room temperature.
- [Camera views](https://github.com/reylinux/Dynamic-Material-Design-3-Inspired-Mobile-Dashboard/blob/main/Camera%20Example.txt) include nearby light toggles for quick control.
- A full weather panel includes [current conditions](https://github.com/reylinux/Dynamic-Material-Design-3-Inspired-Mobile-Dashboard/blob/main/Weather%20Status.txt), warnings, multi-day forecasts, and a live [Windy radar](https://github.com/reylinux/Dynamic-Material-Design-3-Inspired-Mobile-Dashboard/blob/main/Weather%20Radar.txt) embed. You'll need to get the URL from the Windy embed [here](https://embed.windy.com/config/map) and grab the URL within the quotes from the src section and put it in the iframe card.
- Earthquake, volcano, and similar alerts are displayed using dedicated pop-up cards.

# 🧭 Tabbed Navigation per Room
<img width="3200" height="2880" alt="5" src="https://github.com/user-attachments/assets/173aa636-4b7a-4812-ac6c-3e5f3136fd75" />

Rooms are broken into tabs for clear navigation:

- **Room**: Lights and devices
- **Stats**: Temperature and humidity
- **Active**: Open doors/windows, speakers, switches

I use [decluttering_templates](https://github.com/reylinux/Dynamic-Material-Design-3-Inspired-Mobile-Dashboard/blob/main/Decluttering%20Templates.txt) and [button_card_template](https://github.com/reylinux/Dynamic-Material-Design-3-Inspired-Mobile-Dashboard/blob/main/Button%20Card%20Templates.txt) here. Make sure to have the code on top of your dashboard YAML to get them to work. Full code can be found [here](https://github.com/reylinux/Dynamic-Material-Design-3-Inspired-Mobile-Dashboard/blob/main/Living%20Room%20Example.txt)

# 🎨 Scene Selector, Color Palette & Server Info
<img width="3200" height="2880" alt="6" src="https://github.com/user-attachments/assets/1b259be6-8ebe-49dd-9292-607483d5020a" />

- A flexible Philips Hue **scene selector**https://github.com/reylinux/Dynamic-Material-Design-3-Inspired-Mobile-Dashboard/blob/main/Scene%20Example.txt now works independently per room.
- 
  You will need to copy the scripts and automations to get it work. Find the code on the files section.
- A Material You–style color **[palette selector](https://github.com/reylinux/Dynamic-Material-Design-3-Inspired-Mobile-Dashboard/blob/main/Colour%20Palette%20Pop%20Up.txt)** lets you choose from 7 base colors, with real-time UI previews.
- A server overview panel provides key information on hardware setup, uptime, and system performance

Extra credits:
- [Custom weather buttons, Light Slider Cards](https://www.youtube.com/@My_Smart_Home)
- [Windy iFrame](https://www.reddit.com/r/homeassistant/comments/1l4hnx7/weather_dashboard_v100/)

# Sponsor ❤️
[<img width="170" height="37" alt="Buy me a coffee" src="https://github.com/user-attachments/assets/2bc7c798-1015-4293-b674-6680d8413a9c" />](https://buymeacoffee.com/reynaldisuu)
