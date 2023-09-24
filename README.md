from IPythondisplay import HTML, display
from urllib.request import urlopen

CSS_URL = "https://raw.githubusercontent.com/tivendren/mycustomjupytertheme/main/custom.css"
CSS = urlopen(CSS_URL)
CSS = CSS.read().decode('utf-8')
HTML_CSS = f"""
<style>
{CSS}
</style>
"""
HTML(HTML_CSS)
