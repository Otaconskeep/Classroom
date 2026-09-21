# Lesson 08: ESPHome, Zigbee, Matter & Thread

_Build a mesh backbone. Thread tip for Kwikset locks._

Use Zigbee/Z-Wave/ESPHome for gear you need dependable. Let Matter/Thread grow in — do not bet the whole house on it on day one.

## ESPHome before random MQTT

ESPHome gives native HA sensors, switches, displays, Bluetooth proxies, and voice devices with a push-based API (low latency). Learn it before spending weeks on custom MQTT devices.

**What's this mean?** ESPHome is a friendly kit that already speaks Home Assistant’s language. MQTT can wait until you need weird custom talk.

**More detail:** HA ESPHome integration docs. Flash one temperature sensor end-to-end before a drawer of boards.

## Zigbee is a mesh, not just a stick

The USB coordinator is the brain. Mains-powered routers (often smart plugs) form the backbone. Battery sensors are usually end devices. Add routers for coverage. Keep the stick away from USB 3 ports and Wi-Fi radio noise.

**What's this mean?** Battery sensors are quiet mice. Wall-powered plugs are the hallways they run through. One lonely stick in a metal cabinet makes a weak maze.

**More detail:** <div class="cr-flow">Coordinator → smart plugs / repeaters → motion / contact / buttons</div>Official ZHA documentation.

## Matter + Thread — and Kwikset locks

Thread is a low-power mesh used by many Matter devices (including some smart locks). Home Assistant’s Thread network management is still evolving (preferred network, multiple vendors’ border routers). Prefer Zigbee/Z-Wave/ESPHome for must-work infrastructure while Matter/Thread matures in your home.

**What's this mean?** Thread is a special radio neighborhood some new locks join. Matter is the shared language. Your house also needs a border router (like a hub that translates Thread to your Wi-Fi/HA world).

**More detail:** <div class="cr-callout tip"><strong>Kwikset / Thread lock tip:</strong> Many newer Kwikset Home Connect / Aura-class Matter locks expect a working <strong>Thread border router</strong> on your network (examples people use: Apple HomePod mini / TV 4K, certain Nest hubs, or other Matter/Thread BR devices — check the lock’s current pairing guide). Home Assistant alone seeing Wi-Fi is not enough if the lock is Thread-only. Pair with the vendor’s instructions, confirm the Thread network HA should use, and do not skip the border router. If Thread pairing fails, verify BR is online, phone is on 2.4 GHz near the lock, and you are not fighting two preferred Thread networks.</div>
<ul><li>Official HA Thread documentation</li><li>Keep mission-critical locks on a tech you already trust if Thread BR is not ready</li></ul>

## Sources

- [HA ESPHome](https://www.home-assistant.io/integrations/esphome/)
- [HA ZHA](https://www.home-assistant.io/integrations/zha/)
- [HA Thread](https://www.home-assistant.io/integrations/thread/)
