# simple_plotly_dsbrd
import plotly.express as px
df = px.data.gapminder()
fig = px.scatter(
    df,
    x='gdpPercap',
    y='lifeExp',
    size='pop',
    color='continent',
    hover_name='country',
    log_x=True,
    size_max=40,
    animation_frame='year',
    animation_group='country',
    title='ВВП стран с 1952 по 2007 годы',
    labels={'gdpPercap': 'GDP', 'lifeExp': 'Life'}
)
fig.show()
