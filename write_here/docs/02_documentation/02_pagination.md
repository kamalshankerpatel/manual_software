**pagination**

add the following function into the script

```js

document.addEventListener("DOMContentLoaded",function () {

    const itemsPerPage = 4; // Number of items per page

    let currentPage = 1;

    const resourceCards = document.querySelectorAll(".resources-blog-post-card");

    const totalPages = Math.ceil(resourceCards.length / itemsPerPage);

    console.log(resourceCards.length);

  

    function showPage(page) {

      const start = (page - 1) * itemsPerPage;

      const end = start + itemsPerPage;

  

      resourceCards.forEach((card, index) => {

        card.style.display = index >= start && index < end ? "block" : "none";

      });

  

      // Update page number

      document.getElementById("page-number").textContent = `Page ${page}`;

  

      // Enable/Disable buttons

      document.getElementById("prev-page").disabled = page === 1;

      document.getElementById("next-page").disabled = page === totalPages;

    }

  

    // Event Listeners for Pagination Buttons

    document.getElementById("prev-page").addEventListener("click", function () {

      if (currentPage > 1) {

        currentPage--;

        showPage(currentPage);

      }

    });

  

    document.getElementById("next-page").addEventListener("click", function () {

      if (currentPage < totalPages) {

        currentPage++;

        showPage(currentPage);

      }

    });

});

  

    // Show the first page initially

    showPage(currentPage);

  
  

```

  

add the following into the html on the bottom of cards area

  

```HTML

        <div class="pagination-container">

          <button id="prev-page" class="pagination-btn" disabled>Previous</button>

          <span id="page-number">Page 1</span>

          <button id="next-page" class="pagination-btn">Next</button>

        </div>

```