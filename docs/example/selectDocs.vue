<template>
  <div class="bs-docs-section" id="select">
    <h1 class="page-header"><a href="#select" class="anchor">Select</a></h1>
    <p>
      This a <a target="_blank" href="https://silviomoreto.github.io/bootstrap-select/">bootstrap-select</a> implementation.
    </p>
    <div class="bs-example">
      <p>
        <pre>
Select data : {{single}}
        </pre>
      </p>
      <v-select value="{{@single}}">
        <v-option value="Apple"></v-option>
        <v-option value="Banana"></v-option>
        <v-option value="Cherry"></v-option>
        <v-option value="Orange"></v-option>
        <v-option value="Grape"></v-option>
      </v-select>
      <hr>
      <h4>Multiple select</h4>
      <p>
        <pre>
Select data : {{multiple.join(', ')}}
        </pre>
      </p>
      <v-select multiple value="{{@multiple}}">
        <v-option value="Apple"></v-option>
        <v-option value="Banana"></v-option>
        <v-option value="Cherry"></v-option>
        <v-option value="Orange"></v-option>
        <v-option value="Grape"></v-option>
      </v-select>
      <hr>
      <h4>Multiple select limit</h4>
      <p>
        <pre>
Select data : {{multipleLimit.join(', ')}}
        </pre>
      </p>
      <v-select multiple limit="2" value="{{@multipleLimit}}">
        <v-option value="Apple"></v-option>
        <v-option value="Banana"></v-option>
        <v-option value="Cherry"></v-option>
        <v-option value="Orange"></v-option>
        <v-option value="Grape"></v-option>
      </v-select>
      <hr>
      <h4>Custom template</h4>
      <p>
        <pre>
Select data : {{custom.join(', ')}}
        </pre>
      </p>
      <v-select multiple value="{{@custom}}">
        <v-option value="Star"><span class="glyphicon glyphicon-star"></span> Star</v-option>
        <v-option value="Heart"><span class="glyphicon glyphicon-heart"></span> Heart</v-option>
        <v-option value="Film"><span class="glyphicon glyphicon-film"></span> Film</v-option>
        <v-option value="Inbox"><span class="glyphicon glyphicon-inbox"></span> Inbox</v-option>
      </v-select>
    </div>
    <pre><code class="language-markup"><script type="language-mark-up">
<v-select>
  <v-option value="Apple"></v-option>
  <v-option value="Banana"></v-option>
  <v-option value="Cherry"></v-option>
  <v-option value="Orange"></v-option>
  <v-option value="Grape"></v-option>
</v-select>
<hr>
<v-select multiple>
  <v-option value="Apple"></v-option>
  <v-option value="Banana"></v-option>
  <v-option value="Cherry"></v-option>
  <v-option value="Orange"></v-option>
  <v-option value="Grape"></v-option>
</v-select>
<hr>
<v-select multiple limit="2">
  <v-option value="Apple"></v-option>
  <v-option value="Banana"></v-option>
  <v-option value="Cherry"></v-option>
  <v-option value="Orange"></v-option>
  <v-option value="Grape"></v-option>
</v-select>
<hr>
<v-select multiple>
  <v-option value="Star"><span class="glyphicon glyphicon-star"></span> Star</v-option>
  <v-option value="Heart"><span class="glyphicon glyphicon-heart"></span> Heart</v-option>
  <v-option value="Film"><span class="glyphicon glyphicon-film"></span> Film</v-option>
  <v-option value="Inbox"><span class="glyphicon glyphicon-inbox"></span> Inbox</v-option>
</v-select>
    </script></code></pre>
    <h2>Select Options</h2>
    <table class="table table-bordered">
      <thead>
        <tr>
          <th>Name</th>
          <th>Type</th>
          <th>Default</th>
          <th>Description</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>value</td>
          <td><code>Array</code></td>
          <td><code>[]</code></td>
          <td></td>
        </tr>
        <tr>
          <td>placeholder</td>
          <td><code>String</code></td>
          <td>Nothing Selected</td>
          <td></td>
        </tr>
        <tr>
          <td>multiple</td>
          <td><code>Boolean</code></td>
          <td><code>false</code></td>
          <td></td>
        </tr>
        <tr>
          <td>limit</td>
          <td><code>Number</code></td>
          <td><code>1024</code></td>
          <td>Limit the number of elements you are allowed to select.</td>
        </tr>
      </tbody>
    </table>

  </div>
</template>

<script>
  import vSelect from 'src/Select'
  import vOption from 'src/Option'
  export default {
    components: {
      vSelect,
      vOption
    },
    data() {
      return {
        single: [],
        multiple: [],
        multipleLimit: [],
        custom: []
      }
    }
  }
</script>
