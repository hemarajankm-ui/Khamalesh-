# Khamalesh-
Smart AI Farming App for Tamil Nadu
<!-- Feature 2: Crop Disease Detection -->
<div class="feature-card" style="background: white; padding: 20px; border-radius: 12px; box-shadow: 0 4px 6px rgba(0,0,0,0.05); margin-bottom: 15px;">
    <div style="font-size: 24px; margin-bottom: 10px;">🌿</div>
    <h3 style="font-size: 18px; color: #1b4d3e; margin-bottom: 5px;">2. பயிர் நோய் கண்டறிதல்</h3>
    <p style="font-size: 14px; color: #666; margin-bottom: 15px;">பயிரின் புகைப்படத்தைப் பதிவேற்றி நோயைக் கண்டறியுங்கள்</p>
    
    <!-- Image Upload / Camera Input -->
    <div style="border: 2px dashed #4CAF50; padding: 15px; border-radius: 8px; text-align: center; background: #f9f9f9;">
        <input type="file" id="cropImageInput" accept="image/*" capture="environment" style="display: none;" onchange="handleCropImage(event)">
        <label for="cropImageInput" style="cursor: pointer; color: #2e7d32; font-weight: bold; display: block;">
            📷 புகைப்படம் எடுக்க / பதிவேற்ற இங்கே அழுத்தவும்<br>
            <span style="font-size: 12px; color: #555;">(Tap here to take photo or upload)</span>
        </label>
    </div>

    <!-- Results Display Area -->
    <div id="diseaseResult" style="margin-top: 15px; display: none; padding: 10px; background: #e8f5e9; border-radius: 6px;">
        <h4 style="color: #2e7d32; margin-bottom: 5px;" id="resultTitle">மதிப்பீடு செய்கிறது... (Analyzing...)</h4>
        <p style="font-size: 13px; color: #333;" id="resultDesc">தயவுசெய்து காத்திருக்கவும்.</p>
    </div>
</div>

<script>
function handleCropImage(event) {
    const file = event.target.files[0];
    if (file) {
        const resultDiv = document.getElementById('diseaseResult');
        const titleEl = document.getElementById('resultTitle');
        const descEl = document.getElementById('resultDesc');
        
        resultDiv.style.display = 'block';
        titleEl.innerText = "🔍 AI ஆய்வு செய்கிறது... (Analyzing Image)";
        descEl.innerText = "பயிர் இலையை ஸ்கேன் செய்து கொண்டிருக்கிறது. சிறிது நேரம் காத்திருக்கவும்...";

        // Simulating AI analysis response (You can later connect this to a vision API)
        setTimeout(() => {
            titleEl.innerText = "⚠️ இலை புள்ளி நோய் கண்டறியப்பட்டது (Leaf Spot Detected)";
            descEl.innerText = "தீர்வு: சூடோமோனாஸ் (Pseudomonas) அல்லது காப்பர் ஆக்ஸிகுளோரைடு தெளிக்கவும். (Remedy: Spray Pseudomonas or copper oxychloride).";
        }, 2000);
    }
}
</script>
