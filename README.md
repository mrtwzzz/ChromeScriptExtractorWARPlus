# ChromeScriptExtractorWARPlus

📄 README: ScriptExtractor WAR Toolchain
=======================================

🛡️ Fullverdig verktøysett for script-uttrekk, deobfuskering og sanntidsovervåkning

✅ Inkluderte verktøy:

1. ScriptExtractor_CLI_WAR_Pipeline.py
   - Full auto: extraction + deobfuscation + packaging
   - Kjør med:
     python ScriptExtractor_CLI_WAR_Pipeline.py https://target.com

2. ScriptExtractor_CLI_WAR_Deobfuscator.py
   - Brukes på eksportert mappe (inline/dynamic)
     python ScriptExtractor_CLI_WAR_Deobfuscator.py ./inline ./deobfuscated/

3. ScriptExtractor_LiveMonitor.py
   - Sanntidsovervåker DOM for nye/endrede scripts
     python ScriptExtractor_LiveMonitor.py https://target.com

📦 Outputstruktur:

- /external/       → Eksterne scripts (som URL)
- /inline/         → Inline <script> innhold
- /dynamic/        → Eval/innerHTML/mutate funn
- /deobfuscated/   → Dekodet payload (hex/base64/eval)
- metadata.json    → Script-oversikt
- deobfuscated_metadata.json → Dekodingsrapport
- live_monitor_log.json → Sanntidsovervåkingslogg
- /live_dumps/     → Script-filer funnet live

🛠️ Installasjon:
------------------
Kjør:
  pip install -r requirements.txt

Innhold i requirements.txt:
---------------------------
pyppeteer
aiofiles

🚀 Bruksmønster:
----------------
1. Kjør `field_toolkit_installer.sh`
2. Kjør pipeline mot mål
3. Bruk live monitor for runtime-analyse
4. Bruk deobfuscator for dyp reverse
5. Analyser offline med VSCode/Chef etc.

☠️ Ansvar:
---------
Kun for etisk, kontrollert bruk. All bruk skjer på eget ansvar.
