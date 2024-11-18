---
layout: default
title: Search Results
---

## Search Results

<div id="results">
    <!-- Results will be populated here using JavaScript -->
</div>

<script>
document.addEventListener('DOMContentLoaded', function() {
    const urlParams = new URLSearchParams(window.location.search);
    const query = urlParams.get('q');
    
    if (query) {
        document.getElementById('results').innerHTML = `
            <h3>Showing results for: ${query}</h3>
            <div class="popular-destinations">
                <div class="destination">
                    <img src="https://images.unsplash.com/photo-1589979481223-deb893043163?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8Mnx8a2V5JTIwd2VzdHxlbnwwfHwwfHx8MA%3D%3D&auto=format&fit=crop&w=500&q=60" alt="Sample Destination">
                    <h3>Sample Destination in ${query}</h3>
                    <p>Experience the beauty of ${query}</p>
                </div>
                <div class="destination">
                    <img src="https://images.unsplash.com/photo-1501594907352-04cda38ebc29?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8M3x8c2FuJTIwZnJhbmNpc2NvfGVufDB8fDB8fHww&auto=format&fit=crop&w=500&q=60" alt="Another Destination">
                    <h3>Another Spot in ${query}</h3>
                    <p>Discover hidden gems in ${query}</p>
                </div>
            </div>
        `;
    } else {
        document.getElementById('results').innerHTML = '<p>No search query provided. Please try your search again.</p>';
    }
});
</script>
