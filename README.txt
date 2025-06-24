<div align="center">
  
# 🎮 GTA5 TikTok Integration  
**Control GTA V via TikTok Live triggers!**

[![Download Latest Release](https://img.shields.io/github/v/release/smeysu/GTA5-TikTok-Integration?style=flat-square&label=Download&color=brightgreen)](https://github.com/smeysu/GTA5-TikTok-Integration/releases)  
[Recommend TikFinity for webhooks](https://tikfinity.zerody.one/) 🌐

</div>

---

## 📦 Installation

1. Ensure **GTA V is closed**.  
2. Download the latest release.  
3. Extract the ZIP.  
4. Copy its contents into your GTA V installation directory (where `GTA5.exe` is located):  
   - Default: `C:\Program Files\Rockstar Games\Grand Theft Auto V`  
   - Steam: `E:\SteamLibrary\steamapps\common\Grand Theft Auto V`  
5. Launch GTA V in **Offline/Story Mode**.  
6. Open [http://127.0.0.1:6721/](http://127.0.0.1:6721/) — you should see:  
   ```
   Its working!
   ```

> ⚠️ After a GTA V update, you'll likely need to reinstall the plugin.

---

## 🌐 Webhook Commands

Trigger events using HTTP requests like:

```
http://127.0.0.1:6721/<command>:<param>
```

Commands are defined in [`GTAVWebhookScript.cs`](https://github.com/smeysu/GTA5-TikTok-Integration/blob/main/GTAVWebhookScript.cs). Here's a quick reference:

- 🎯 `/kill` — Kill the player  
- 🚓 `/spawn_vehicle:Felon` — Spawn a Felon vehicle  
- 🧨 `/explode_vehicle` — Blow up nearby vehicles  
- 🔫 `/give_weapon:CombatMG` — Give Combat MG  
- 💣 `/set_max_weapon_ammo` — Max ammo  
- ⏰ `/set_time:02` — Set time (e.g., 2AM)  
- ☀️ `/set_weather:Raining` — Apply weather (Clear, Clouds, Snowing, etc.)  
- 🚔 `/increase_wanted`, `/decrease_wanted`, `/max_wanted` — Manage wanted levels (1–5)  
- 💵 `/add_money:10`, `/set_money:500` — Adjust cash (use negative for deduction)  
- 👥 `/spawn_attackers:1`, `/spawn_attackers_and_shoot:1` — Spawn (armed) attackers  
- 🔫 `/attackers_start_shooting:30`, `/remove_attackers:5` — Attackers attack or clean up  
- 🚗 `/repair_current_vehicle`, `/remove_spawned_vehicles`, `/leave_car`, `/skydive`  
- ❤️ `/increase_health:20` — Modify health (use negative to reduce)

More commands are coming—check the script file for updates.

---

## 📲 TikFinity Integration

Use [TikFinity](https://tikfinity.zerody.one/) to link TikTok LIVE events with webhooks (free for up to 5):

1. **Create Action**:  
   - Go to *Actions & Events* → *Create new Action* → *Trigger Webhook*.  
   - Paste your webhook URL (e.g. `/spawn_vehicle:Felon`) and save.  
2. **Create Event**:  
   - Click *Create new Event*, set your TikTok trigger (e.g., Gift X), and link it to your webhook action.

Repeat to map more events and commands.

---

## 🛠️ Troubleshooting

Check these log files in your GTAV directory if something breaks:

- `asiloader.log`  
- `ScriptHookV.log`  
- `ScriptHookVDotNet.log`  
- `GTAVWebhook.log`

If `ScriptHookVDotNet` fails to load, ensure [.NET Framework 4.8](https://support.microsoft.com/en-us/topic/microsoft-net-framework-4-8-offline-installer-for-windows-9d23f658-3b97-68ab-d013-aa3c3e7495e0) is installed.

---

## 💬 Support & 👥 Contribute

- **Discord**: Smeys#5697  
- **Pull Requests are welcome!** Expand features, add new webhooks, etc.

---

### 📌 Summary

This plugin lets your TikTok audience directly influence your GTA V gameplay via live events — making streams interactive, chaotic, and fun!
