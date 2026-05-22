# Hardcore Deaths Plugin

Een complete Minecraft Spigot/Paper plugin die hardcore gamemode features toevoegt aan je server!

## Features

- 🔊 **Death sounds** wanneer spelers sterven
- 👻 **Grace period** - Eerste 2 uur automatisch reviven bij dood
- ⏱️ **Spectator mode** - Na grace period: 5 minuten spectator
- 🔨 **Auto-kick** - Na 5 minuten spectator (admins kunnen reviven)
- 📊 **Death statistics** - Alle sterfgevallen gelogd
- 📢 **Broadcasts** - Death messages voor alle spelers
- ⚡ **Multiple commands** - Alles wat je nodig hebt
- 💾 **Admin control** - Revive, config, en meer
- 🎯 **Scoreboard** - Live statistieken in sidebar
- 👥 **Team system** - Team-based gameplay
- 🎪 **Event system** - Speciale events en bounties
- 💤 **AFK system** - AFK detectie en kick
- 🏆 **Challenge system** - Daily challenges
- ⭐ **Premium features** - Extra styling en branding

## Commands

### Voor alle spelers:
- `/AFKcheck` - Bekijk wie er allemaal AFK staat
- `/AFK` - Ga afk en sta stil tot 1 van de admins je kickt
- `/grace` - Bekijk je grace period status
- `/hardcore info` - Plugin informatie
- `/hardcore stats` - Top 10 death statistieken
- `/hardcore status` - Huidge server status
- `/hardcore list` - Wie is aan het spectaten?
- `/premium` - Bekijk premium status en features

### Voor admins:
- `/AFKKick` - Kick players die afk zijn voor hun eige veiligheid.
- `/event` - Start een event die zijn voorgeprogrameerd of die je zelf hebt gemaakt.
- `/broadcast` - Maak een announcement in de chat
- `/reload` - Reload de plugin
- `/revive <speler>` - Revive een dode speler
- `/hardcore config` - Configuratie bekijken
- `/admin` - Open admin control panel
- `/heal [player]` - Heal jezelf of anderen
- `/feed [player]` - Feed jezelf of anderen

## Team System
- `/team create <naam>` - Maak een team
- `/team join <naam>` - Join een team
- `/team leave` - Verlaat je team
- `/team info` - Team informatie
- `/team list` - Alle teams bekijken
- `/team leaderboard` - Team leaderboard
- `/team members` - Team leden bekijken
- `/team disband` - Team ontbinden

## Event System
- `/events list` - Beschikbare events bekijken
- `/events toggle <event>` - Event aan/uit zetten

## Bounty System
- `/bounty set <player> <amount>` - Zet bounty op speler
- `/bounty remove <player>` - Verwijder bounty
- `/bounty list` - Alle bounties bekijken

## Grace Period Systeem

**Eerste 2 uur** dat je op de server speelt:
- Je bent in de **grace period**
- Als je sterft, word je **automatisch gereivived**
- Je krijgt volledige health en hunger terug
- Geen spectator mode!

**Na 2 uur:**
- Grace period eindigt
- Bij sterven ga je naar **spectator mode (5 minuten)**
- Daarna word je **gekicked**
- Admins kunnen je met `/revive` terugnemen

## Building

### Normale build

```bash
mvn clean package
```

Dit genereert de normale plugin:

- `target/Hardcore.jar`

### Beta build

Wil je de eerste/beta variant bouwen, gebruik dan:

```bash
mvn clean package -Pbeta
```

Dit genereert:

- `target/Hardcore-Beta.jar`

### Premium build

Wil je de premium variant bouwen, gebruik dan:

```bash
mvn clean package -Ppremium
```

Dit genereert:

- `target/Premium-Hardcore.jar`

### Bewaar alle builds

Alle builds kopiëren hun resultaat naar:

- `dist/Hardcore.jar`
- `dist/Hardcore-Beta.jar`
- `dist/Premium-Hardcore.jar`

Zo blijven eerdere builds bewaard, ook als je later een andere build uitvoert.

Alle builds blijven dezelfde codebasis delen; de Premium build gebruikt daarnaast een eigen `plugin-premium.yml` voor de premium plugin metadata.

## Config

Alle instellingen kunnen aangepast worden in de Java classes:

- **GracePeriodManager.java** - Grace period duur (standaard 2 uur)
- **SpectatorManager.java** - Spectator duur (standaard 5 minuten)
- **DeathEventListener.java** - Death sound type

## Versie Compatibiliteit

- **Java:** 1.8+
- **Minecraft:** 1.12.2+ (Paper/Spigot)

## Made By Maxineter_

Deze plugin is met liefde gemaakt door Maxineter_ voor de Eurokings Hardcore community!

