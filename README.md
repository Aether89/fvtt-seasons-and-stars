# Seasons & Stars

A modern calendar and timekeeping module for Foundry VTT v13+ with clean integration APIs and extensible architecture.

## 🌟 Features

### ✅ **Available Now (Beta)**
- **Modern UI**: Clean, responsive calendar interface with ApplicationV2 architecture
- **Multiple Calendar Views**: Full calendar widget, compact mini widget, and monthly grid view
- **Smart Year Navigation**: Click year to jump instantly instead of clicking arrows repeatedly
- **Real-World Integration**: Gregorian calendars automatically initialize with current date/time
- **Module Integration**: Clean APIs for weather modules and other integrations via compatibility bridges
- **SmallTime Integration**: Seamless positioning and visual consistency
- **Multiple Calendar Support**: Switch between Gregorian, Vale Reckoning, and custom calendars

### 🚧 **Coming Soon**
- **Notes System**: Full calendar event and note management with Journal integration
- **Weather Module Support**: Comprehensive notes API for weather modules and other integrations
- **Advanced Configuration**: In-app calendar editor and migration tools
- **Extended Integrations**: Enhanced module compatibility and hook system

## 🚀 Quick Start

### Installation
1. Install from Foundry VTT module browser: "Seasons & Stars"
2. Enable the module in your world
3. Configure your preferred calendar in module settings

### Basic Usage
- **Open Calendar**: Click the calendar button in scene controls
- **Change Date**: GMs can click on calendar dates to set world time
- **Quick Time Controls**: Use the mini widget for rapid time advancement
- **Calendar Selection**: Switch between different calendar systems anytime

## 📖 Documentation

- **[User Guide](./docs/USER-GUIDE.md)** - Complete usage instructions
- **[Developer Guide](./docs/DEVELOPER-GUIDE.md)** - API reference and integration guide
- **[Migration Guide](./docs/MIGRATION-GUIDE.md)** - Moving from Simple Calendar
- **[Roadmap](./docs/ROADMAP.md)** - Development timeline and planned features

## 🎯 Who Should Use This

### **Beta Testers**
- Users seeking a modern calendar solution for Foundry v13+
- Module developers wanting to integrate calendar functionality
- GMs who need reliable timekeeping with clean UI

### **Migration Candidates**
- Users seeking a modern calendar solution for Foundry v13+
- Users wanting better SmallTime integration
- Communities needing custom calendar support

## 🤝 Module Integration

Seasons & Stars provides **clean integration APIs** for calendar-aware modules:

```javascript
// Direct API access
const currentDate = game.seasonsStars.api.getCurrentDate();
const worldTime = game.seasonsStars.api.dateToWorldTime(someDate);
const formatted = game.seasonsStars.api.formatDate(currentDate);

// Hook integration for module updates
Hooks.on('seasons-stars:dateChanged', (data) => {
  // Respond to date changes in your module
  console.log('Date changed:', data.newDate);
});
```

**Compatibility bridges available** for seamless migration from other calendar systems.

## 📋 Requirements

- **Foundry VTT**: v13 or higher
- **Compatibility**: All game systems (system-agnostic design)
- **Permissions**: GM required for time changes

## 🔧 Development

### For Module Developers
```javascript
// Access the Seasons & Stars API
const currentDate = game.seasonsStars.api.getCurrentDate();
await game.seasonsStars.api.advanceDays(1);

// Listen for date changes
Hooks.on('seasons-stars:dateChanged', (data) => {
  console.log('Date changed:', data.newDate);
});
```

See the [Developer Guide](./docs/DEVELOPER-GUIDE.md) for complete API reference.

### Build from Source
```bash
git clone https://github.com/your-username/seasons-and-stars
cd seasons-and-stars
npm install
npm run build
```

## 🗺️ Roadmap

### **Phase 1: Core Foundation** ✅ *Complete*
- Basic calendar system and UI
- Simple Calendar compatibility layer
- Essential user features

### **Phase 2: Notes & Integration** 🚧 *Next (Q1 2025)*
- Full notes system with Journal integration
- Complete weather module support
- Advanced hook system

### **Phase 3: Advanced Features** 📅 *Q2 2025*
- Calendar editor and creation tools
- Migration assistant from Simple Calendar
- Enhanced theming and customization

See the complete [Roadmap](./docs/ROADMAP.md) for detailed timelines.

## 📄 License

[MIT License](./LICENSE) - Free for personal and commercial use.

## 🐛 Support & Feedback

- **Issues**: [GitHub Issues](https://github.com/your-username/seasons-and-stars/issues)
- **Discussions**: [GitHub Discussions](https://github.com/your-username/seasons-and-stars/discussions)
- **Discord**: [Foundry VTT Community](https://discord.gg/foundryvtt) - `#modules` channel

---

**Ready to modernize your calendar system?** Install Seasons & Stars today and experience the difference!