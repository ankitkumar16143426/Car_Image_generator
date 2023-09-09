# Car_Image_generator
First we take a container class,afer that we take a button (get car), after that we take a another div , that is car_container, after that we apply basic CSS,
In the JavaScript part we get the button (document.getElementById("btn"))and apply the QuariSelector (document.querySelector(".car-container") ) after that we apply EventListener on button (on click)          btn.addEventListener("click", async function () and apply try catch, in the try we fetch the API and when API gives us the response.we convert responce into json :-
    const data = await response.json();
    btn.innerText = "Get Cars";
    carContainer.style.display = "block";
    carImg.src = data.links.download;
    carName.innerText = data.alt_description;
  and in the catch part we handle the error
  catch (error) {
    console.log(error);
    btn.disabled = false;
    btn.innerText = "Get car";
    carName.innerText = "An error happened, please try again";
