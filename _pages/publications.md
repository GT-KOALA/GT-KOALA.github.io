---
layout: page
permalink: /publications/
title: Publications
description: Publications from the KOALA Lab at Georgia Tech.
nav: true
nav_order: 1
---

<p class="text-muted mb-1">
  Kai Wang's name is <u>underlined</u>. See also
  <a href="https://scholar.google.com/citations?user=spWVns8AAAAJ" target="_blank">Google Scholar</a>.
</p>

<div id="year-filter" class="my-3"></div>

<div class="publications">
{% bibliography %}
</div>

<script>
document.addEventListener('DOMContentLoaded', function () {
  var pubDiv = document.querySelector('div.publications');
  if (!pubDiv) return;

  // al-folio uses h2.bibliography for year group headers
  var yearHeadings = Array.from(pubDiv.querySelectorAll('h2.bibliography'));
  if (yearHeadings.length === 0) return;

  var filterDiv = document.getElementById('year-filter');

  var label = document.createElement('span');
  label.className = 'fw-semibold me-2 align-middle';
  label.textContent = 'Filter by year:';
  filterDiv.appendChild(label);

  filterDiv.appendChild(makeBtn('All', 'all', true));

  yearHeadings.forEach(function (h) {
    var year = h.textContent.trim();
    h.dataset.filterYear = year;
    filterDiv.appendChild(makeBtn(year, year, false));
  });

  filterDiv.addEventListener('click', function (e) {
    var btn = e.target.closest('.year-btn');
    if (!btn) return;

    var selected = btn.dataset.year;

    filterDiv.querySelectorAll('.year-btn').forEach(function (b) {
      b.classList.toggle('active', b.dataset.year === selected);
    });

    yearHeadings.forEach(function (h) {
      var show = selected === 'all' || h.textContent.trim() === selected;
      h.style.display = show ? '' : 'none';
      var sib = h.nextElementSibling;
      while (sib && sib.tagName.toLowerCase() !== 'h2') {
        sib.style.display = show ? '' : 'none';
        sib = sib.nextElementSibling;
      }
    });
  });

  function makeBtn(label, yearKey, active) {
    var btn = document.createElement('button');
    btn.className = 'btn btn-sm btn-outline-secondary year-btn me-1 mb-1' + (active ? ' active' : '');
    btn.dataset.year = yearKey;
    btn.textContent = label;
    return btn;
  }
});
</script>

<style>
#year-filter .year-btn.active {
  background-color: var(--global-theme-color, #0076df);
  color: #fff;
  border-color: var(--global-theme-color, #0076df);
}
#year-filter .year-btn:not(.active):hover {
  background-color: rgba(0, 118, 223, 0.1);
}
</style>
