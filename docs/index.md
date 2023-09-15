
 <title>Local Vehicle Classifier</title>

<input id="photo" type="file">
<div id="results"></div>
<script>
    async function loaded(reader) {   
    const response = await fetch("https://nifulislam-Vehicle-Classifier.hf.space/run/predict", {
        method: "POST", headers: { "Content-Type": "application/json" },
        body: JSON.stringify({data: [reader.result]})});
    const json = await response.json();
    const label = json['data'][0]['label'];
    results.innerHTML = `<br/> <img src = "${reader.result}" width="500"> <p>${label}</p>`;
    }
    function read() {
        const reader = new FileReader();
        reader.addEventListener('load', () => loaded(reader))
        reader.readAsDataURL(photo.files[0]);
    }
    photo.addEventListener('input', read);
</script>


# Image Classifier
This image classifier can classify 6 tyepes of local vehicles. The types are: <br>
1. Bike
2. Truck
3. Bicycle
4. Car
5. Boat
6. Easy-bike


