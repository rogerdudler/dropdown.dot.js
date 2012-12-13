# dropdown.dot.js #

A super-flexible and clean JQuery Dropdown Plugin based on dot.js Templates.

# Use default markup as your data source and reference a dot template # #

    <select data-template="#dropdown">
        <option value="1" selected="selected">Super</option>
        <option value="2">Awesome</option>
        <option value="3">Dropdown</option>
    </select>

# Use dot.js Templates for your Dropdown #

    <script id="dropdown-selected" type="text/x-dot-template">
    {{=data.label}}<div class="arrow"><i></i></div>
    </script>
    <script id="dropdown" type="text/x-dot-template">
    <div class="dropdown" tabindex="1">
        <div class="selected">{{=data.selected.label}}</div>
        <ul>
            {{~data.items :item:index}}
            <li data-index="{{=index}}">{{=item.label}}</li>
            {{~}}
        </ul>
    </div>
    </script>

# Usage #

    $('select').dropdown();

# Credits #

Coded by Roger Dudler
http://twitter.com/rogerdudler