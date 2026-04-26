# 🚪 Klingel — Türklingel via QR-Code

Landing-Page für QR-Code-Türklingel — gehört zu **NOVA Sprach-Assistent** (GZ-AI.-Stacks).

## Wie funktioniert's

1. Besucher steht vor der Tür → scannt QR-Code → diese Seite öffnet sich
2. Tippt optional Namen + Nachricht ein → klickt "🔔 KLINGELN"
3. NOVA bekommt Live-Push → spielt Klingel-Sound + TTS-Ansage
4. Du weißt sofort wer/was vor der Tür ist

## Setup

### 1. Tunnel-URL eintragen
Wenn dein Cloudflare-Tunnel sich ändert (z.B. nach NOVA-Neustart), in `tunnel.json` aktualisieren:

```json
{
  "nova_url": "https://deine-aktuelle-tunnel-url.trycloudflare.com"
}
```

→ commit + push → fertig (1 Min Aufwand pro Tunnel-Wechsel)

### 2. URL für QR-Code
```
https://gz-ai-stacks.github.io/klingel/?owner=Gerd&token=DEIN_TOKEN&phone=49xxx
```

Parameter:
- `owner` — dein Name (wird auf der Page angezeigt)
- `token` — Geheim-Token aus NOVA (Spam-Schutz)
- `phone` — deine Telefonnummer für die "📞 Anrufen"/"💬 WhatsApp" Buttons (optional)

Den Token findest du in NOVA: Quick-Command "🚪 Türklingel" → Tab "⚙ Einstellungen".

### 3. QR-Code generieren
In NOVA: Quick-Command "🚪 Türklingel" → Tab "🔲 QR-Code" → Drucken oder Kopieren.

## Privacy

- Klingel-Page läuft komplett im Browser des Besuchers
- Keine Daten werden hier gespeichert
- Keine Cookies, kein Tracking
- Klingel-Daten gehen direkt zu deinem NOVA-Server (Cloudflare-Tunnel, end-to-end)

## Lizenz

(c) Gerd Zimmermann · GZ-AI.-Stacks · MIT-Lizenz
