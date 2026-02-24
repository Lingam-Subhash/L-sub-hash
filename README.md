<div style="
  background:#0d1117;
  padding:20px;
  border-radius:10px;
  font-family:monospace;
  color:#c9d1d9;
  white-space:pre-line;
">
<span id="terminal"></span><span id="cursor">▌</span>
</div>

<script>
const lines = [
  "subhash@subu:~$ whoami",
  "Subhash",
  "",
  "Penetration testing student with an offensive mindset.",
  "I analyze systems by probing, breaking, and tracing failure paths across networks and applications.",
  "",
  "My work revolves around reconnaissance, OSINT, vulnerability discovery, and exploit reasoning — tested in controlled lab environments.",
  "I focus on how systems fail under real conditions, not how tools claim they should work."
];

let lineIndex = 0;
let charIndex = 0;
const speed = 35;

function type() {
  const terminal = document.getElementById("terminal");

  if (lineIndex < lines.length) {
    if (charIndex < lines[lineIndex].length) {
      terminal.textContent += lines[lineIndex].charAt(charIndex);
      charIndex++;
      setTimeout(type, speed);
    } else {
      terminal.textContent += "\n";
      lineIndex++;
      charIndex = 0;
      setTimeout(type, 400);
    }
  }
}

type();
</script>
