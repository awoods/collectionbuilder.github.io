<div class="text-center">
  <figure class="figure {{ include.class }}">
    <img src="{{ include.img | prepend: '/images/' | absolute_url }}" class="figure-img img-fluid rounded border" alt="{{ include.caption }}">
    <figcaption class="figure-caption">{{ include.caption }}</figcaption>
  </figure>
</div>