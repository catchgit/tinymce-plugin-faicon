# tinymce-plugin-faicon
A plugin for MODX TinyMCE that adds the option to place a Font Awesome icon.
<img width="801" height="70" alt="image" src="https://github.com/user-attachments/assets/3639eef9-1c92-471a-b7a3-d32ee45a90be" />
<img width="513" height="396" alt="image" src="https://github.com/user-attachments/assets/862b83e8-efea-49eb-91ae-624dfbc03dd6" />

Tested with MODX 3.1.2 and TinyMCE Rich Text Editor 3.1.5
Tested with Font Awesome 7 & 6 Free or Pro

You need to do three things to activate it:

1. Add "faicon" to the system setting tinymcerte.plugins
2. Add "faicon" to the toolbar setting, for example tinymcerte.toolbar1
3. Add "{"extended_valid_elements": "i[*]"}" to tinymcerte.settings

You will also need somehow to load Font Awesome into the backend (both the editor and Manager):

1. Editor: Add path-to-fontawesome.css to tinymcerte.content_css
2. Manager: Use a plugin to inject FontAwesome CSS, for example:

<pre lang="markdown">
  if ($modx->event->name == 'OnManagerPageBeforeRender') {
    $modx->regClientCSS('path-to-fontawesome.css');
  }
</pre>
