<script src="https://unpkg.com/launchdarkly-js-client-sdk@2.18.1/dist/ldclient.min.js"></script>

<h1> Laks' Contract Project </h1>

<iframe width="1280" height="720" src="https://www.youtube.com/embed/_wHJNT0-OEQ" title="Jaan Ban Gaye - Lyrical | Khuda Haafiz | Vidyut J | Shivaleeka O | Mithoon Ft. Vishal M, Asees Kaur" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<iframe width="1903" height="786" src="https://www.youtube.com/embed/XpF4YJ4W1jo" title="Tamil Drama : Sowmya Theatres  presents IRAIVAN KODUTHA VARAM  by T.V.Radhakrishnan" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<div id="preview" style="display: none">
<iframe width="1903" height="786" src="https://www.youtube.com/embed/GGaIDTqmFbQ" title="Tamil Drama - Dummies presents ‘NALLATHOR VEENAI by V.Sreevathson" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

<script>
var clientid = "62c57a035a57c715df92c2bf";
var flagName = "course-preview";
var user = {anonymous: true};
var ldClient = window.LDClient.initialize(clientid, user);

ldClient.on("ready", function () {
    document.getElementById("preview").style.display = ldClient.variation(flagName, false) ? "block":"none";

});

ldClient.on("change:" + flagName, function (newVal, preVal) {
    document.getElementById("preview").style.display = newVal ? "block":"none";
});

</script>