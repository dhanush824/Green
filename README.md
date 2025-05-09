<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Green Skills Tracker</title>
</head>
<body>
    <h1>Green Skills Education Tracker</h1>
    <ul>
        {% for course in courses %}
            <li>
                {{ course.name }} -
                {% if course.completed %}
                    ✅ Completed
                {% else %}
                    <a href="/complete/{{ loop.index0 }}">Mark as complete</a>
                {% endif %}
            </li>
        {% endfor %}
    </ul>
</body>
</html>
