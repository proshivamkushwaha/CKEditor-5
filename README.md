# CKEditor-5
**On application.br file.**
```<script src="https://cdn.ckeditor.com/ckeditor5/34.1.0/classic/ckeditor.js"></script>```

**On your create.html.erb or _form.html.erb File** 
```<!DOCTYPE html>
<html>
<head>
        <meta charset="utf-8">
        <title>CKEditor</title>
        <script src="https://cdn.ckeditor.com/ckeditor5/34.1.0/classic/ckeditor.js"></script>
</head>
<body>

  <div>
    <%= form.label :title, style: "display: block" %>
    <%= form.text_field :title %>
  </div>

    <%= form.label :body, style: "display: block" %>
    <%= form.text_area :body, id: "editor" %>

  <script>
    ClassicEditor
            .create( document.querySelector( '#editor' ) )
            .then( editor => {
                    console.log( editor );
            } )
            .catch( error => {
                    console.error( error );
            } );
  </script>
</body>
</html>```

**On your show.html.erb**
```<div id="<%= dom_id post %>">
  <p>
    <strong>Title:</strong>
    <%= post.title %>
  </p>

  <p>
    <strong>Body:</strong>
    <%= raw post.body %>
  </p>
</div>```
      


