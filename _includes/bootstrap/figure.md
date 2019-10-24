<figure class="figure {{include.class}}">
  <img src="{{ include.img | prepend: '/images/' | absolute_url }}" class="figure-img img-fluid rounded" alt="{{include.caption}}">
  <figcaption class="figure-caption">{{ include.caption }}</figcaption>
</figure>