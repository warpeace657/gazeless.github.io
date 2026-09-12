<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gazeless: The Blinder Dashboard</title>
    <style>
        :root { --bg-dark: #121212; --panel-bg: #1e1e1e; --text-main: #e0e0e0; --crimson: #b30000; --sky-blue: #4da6ff; --hollow-gray: #777777; }
        body { font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif; background-color: var(--bg-dark); color: var(--text-main); margin: 0; padding: 15px; box-sizing: border-box; }
        .header { text-align: center; border-bottom: 2px solid var(--panel-bg); padding-bottom: 15px; margin-bottom: 20px; }
        .title { font-size: 24px; font-weight: bold; letter-spacing: 2px; margin: 0; }
        .subtitle { font-size: 12px; color: var(--hollow-gray); letter-spacing: 4px; text-transform: uppercase; margin-top: 5px; }
        .tabs { display: flex; gap: 5px; margin-bottom: 15px; background: #000; padding: 5px; border-radius: 8px; }
        .tab { flex: 1; text-align: center; padding: 10px 5px; font-size: 12px; font-weight: bold; border-radius: 6px; cursor: pointer; border: none; background: transparent; color: var(--hollow-gray); }
        .tab.active { background: var(--panel-bg); color: #fff; }
        .panel { background: var(--panel-bg); border-radius: 12px; padding: 20px; display: none; box-shadow: 0 4px 10px rgba(0,0,0,0.3); }
        .panel.active { display: block; }
        h3 { margin-top: 0; display: flex; align-items: center; gap: 10px; }
        .crimson-txt { color: var(--crimson); } .blue-txt { color: var(--sky-blue); } .hollow-txt { color: #fff; }
        ul { padding-left: 20px; margin: 10px 0; }
        li { margin-bottom: 10px; line-height: 1.4; }
        .badge { display: inline-block; padding: 3px 8px; font-size: 10px; font-weight: bold; border-radius: 4px; text-transform: uppercase; margin-top: 5px; }
        .bg-crimson { background: rgba(179,0,0,0.2); color: var(--crimson); border: 1px solid var(--crimson); }
        .bg-blue { background: rgba(77,166,255,0.2); color: var(--sky-blue); border: 1px solid var(--sky-blue); }
        .bg-hollow { background: rgba(119,119,119,0.2); color: #fff; border: 1px solid var(--hollow-gray); }
    </style>
</head>
<body>

    <div class="header">
        <div class="title">GAZELESS</div>
        <div class="subtitle">The Blinder</div>
    </div>

    <div class="tabs">
        <button class="tab active" onclick="switchTab('gazes')">THE GAZES</button>
        <button class="tab" onclick="switchTab('messengers')">MESSENGERS</button>
        <button class="tab" onclick="switchTab('endings')">END ROUTES</button>
    </div>

    <!-- TAB 1: THE GAZES -->
    <div id="gazes" class="panel active">
        <h3 class="crimson-txt">🔴 The Crimson Gaze</h3>
        <p><strong>The Age of the Flayed Horizon:</strong> A blood-red sun eye locks at the zenith. Passive stamina regen is disabled—you must hit exposed enemy weaknesses to recover energy. Lethality is dangerously high for both you and monsters.</p>
        
        <h3 class="blue-txt">🙈 The Averting Gaze</h3>
        <p><strong>The Age of the Blind Zenith:</strong> An eerie, permanent clear sky-blue noon. The world looks pristine, but structures are illusory. Hitboxes hide grotesque true shapes. Requires precise rhythmic memory to survive.</p>
        
        <h3 class="hollow-txt">🌑 The Hollow Gaze</h3>
        <p><strong>The Age of the Ashen Canvas:</strong> A black hole void draining all color and elements. Focuses entirely on weight, momentum, and poise. Glitched terrain fragments from the other two gazes intersect the plains.</p>
    </div>

    <!-- TAB 2: MESSENGERS -->
    <div id="messengers" class="panel">
        <h3 class="crimson-txt">🐛 The Crimson Flayed Scholar</h3>
        <p>A giant, non-human, segmented biological centipede creature that wraps around the checkpoints, violently piercing your flesh to channel levels and strength.</p>
        
        <h3 class="blue-txt">🪷 The Nun of the Blue Lily</h3>
        <p>A serene, white-veiled priestess with blue spider lilies blooming directly out of her empty eye sockets. Offers blind amnesia and deceptive, warm comfort.</p>
        
        <h3 class="hollow-txt">🧵 The Stitched Devotee</h3>
        <p>A multi-mouthed eldritch woman whose joints tear open to reveal stretching flesh. She is completely hollow, obsessed with you, and views you as her entire reality.</p>
    </div>

    <!-- TAB 3: ENDINGS -->
    <div id="endings" class="panel">
        <h3 class="crimson-txt">🔴 Crimson Gaze Branches</h3>
        <ul>
            <li><strong>The Flayed Tyrant:</strong> Enforce total submission to raw truth. No comfort or secrets remain; humanity decays in the light.</li>
            <li><strong>The Fractured Lens:</strong> The sun shatters into individual eyes embedded in every mortal's flesh. Decentralized anarchy.</li>
            <li><strong>The Martyr's Veil:</strong> You filter the red sun through your own body, giving humanity enough shadow to rebuild.</li>
        </ul>
        
        <h3 class="blue-txt">🙈 Averting Gaze Branches</h3>
        <ul>
            <li><strong>Golden Anesthesia:</strong> The lie locks completely. Humanity dances in bliss while their real bodies rot to ash.</li>
            <li><strong>The Cracking Mirror:</strong> The clear sky blue breaks with glowing structural cracks, causing the illusion to violently glitch.</li>
            <li><strong>The Inherited Dream:</strong> You kill the god, claim its empty throne, and cast a tailor-made paradise of your own design.</li>
        </ul>
    </div>

    <script>
        function switchTab(tabId) {
            document.querySelectorAll('.panel').forEach(p => p.classList.remove('active'));
            document.querySelectorAll('.tab').forEach(t => t.classList.remove('active'));
            document.getElementById(tabId).classList.add('active');
            event.target.classList.add('active');
        }
    </script>
</body>
</html>
