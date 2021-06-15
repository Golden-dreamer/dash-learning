# -*- coding: utf-8 -*-
#!/usr/bin/env python3
"""
Created on Tue Jun 15 06:49:50 2021

@author: leo
"""

import dash
import dash_core_components as dcc
import dash_html_components as html
import plotly.express as px
import pandas as pd

external_styesheets = ['https://codepen.io/chriddyp/pen/bWLwgP.css']

app = dash.Dash(__name__, external_stylesheets=external_styesheets)

df = pd.DataFrame({
    "Fruit": ["Apples", "Oranges", "Bananas", "Apples", "Oranges", "Bananas"],
    "Amount": [4, 1, 2, 2, 4, 5],
    "City": ["SF", "SF", "SF", "Montreal", "Montreal", "Montreal"]
})

fig = px.bar(df, x='Fruit', y='Amount', color='City', barmode='group')

app.layout = html.Div(children=[
    html.H1(children='Hello Dash'),
    html.Div(children='''
             This is first hello-world project with dash
             '''),
    dcc.Graph(
        id='example-graph',
        figure=fig
        )
    ])

if __name__ == '__main__':
    app.run_server(debug=True)
