# Lesson 07: Home Assistant: learn it in order

_Devices → integrations → automations. Backups before fancy._

Home Assistant OS is the recommended install for most people. Learn layers in order so automations make sense.

## The learning ladder

Devices → Integrations → Entities → Areas → Helpers → Scenes → Scripts → Automations → Blueprints → Templates → Voice / Assist.

**What's this mean?** First plug things in. Then name them. Then group rooms. Then write “when this happens, do that.” Voice comes last — after the house already listens to plain automations.

**More detail:** Official Getting Started + full docs. NetworkChuck’s HA video is a friendly tour into Zigbee sensors and household automations.

## Automations mental model

TRIGGER → CONDITION → ACTION. Newer HA releases use clearer purpose wording in the editor, but the model is the same.

**What's this mean?** When the door opens (trigger), if it is night (condition), turn on the lamp (action). Three Lego bricks.

**More detail:** Read Automation documentation, Understanding automations, and the Automation editor. Practice with one lamp before twenty conditions.

## Backups and security first

Turn on automatic backups in the UI before deep customization. Use strong unique passwords, MFA, updates, limited admin accounts, and secure remote access (Tailscale/ZeroTier or HA Cloud — not a naked port forward).

**What's this mean?** Save a restore point before you redecorate. Lock the doors before you add more gadgets.

**More detail:** Official HA backups, securing Home Assistant, and remote access docs.

## Sources

- [HA Getting Started](https://www.home-assistant.io/getting-started/)
- [HA Automations](https://www.home-assistant.io/docs/automation/)
- [HA Remote access](https://www.home-assistant.io/docs/authentication/)
