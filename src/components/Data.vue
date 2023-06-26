<template>
    <div id="thisPart">
        
    </div>
  </template>
  <script>
  async function UserData() {
    const data = await fetch(
      "https://eightonleepaulse12.github.io/JSON-SERVER/database/anime.json"
    );
    const jsonData = await data.json();
    console.log(jsonData);
    let newData = jsonData.anime
    const display = document.querySelector("#thisPart");
    newData.forEach((data) => {
      display.innerHTML += `
        <div class="card">
          <div class="card-body">
            <h3 class="card-title">${data.name}, ${data.author}</h3>
            <img src=${data.picture}>
            </div>
          </div>
        `;
    });
  }
  UserData();
  </script>
  <style>
  </style>
  