# dropdown.dot.js

A super-flexible and clean JQuery Dropdown Plugin based on dot.js Templates.

# Markup

    <select data-template="#dropdown">
        <option value="1" selected="selected">Super</option>
        <option value="2">Awesome</option>
        <option value="3">Dropdown</option>
    </select>

# dot.js Templates

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

# Basic Usage

    $('select').dropdown();

# Add additional data to your markup #

For example you want to add a ```count``` for every item to show in the select menu next to the label.

    <select data-template="#dropdown">
        <option value="1" data-count="2" selected="selected">Super</option>
        <option value="2" data-count="5">Awesome</option>
        <option value="3" data-count="1">Dropdown</option>
    </select>

# ... and use it in your template with

    {{=item.count}}

# Credits

Coded by Roger Dudler
http://twitter.com/rogerdudler