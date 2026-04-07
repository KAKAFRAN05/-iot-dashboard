import pandas as pd
import streamlit as st
url = "https://docs.google.com/spreadsheets/d/e/2PACX-1vS1xQHjjdkbAyidZ8Ab3DpjOtQ9xy1Anhg7VyPdpHOmz08_bxidxiHyzsxr6QSHsRQptepVlFksybns/pub?gid=0&single=true&output=csv"
df = pd.read_csv(url)
st.title("Monitoramento IoT")
st.line_chart(df[['temperatura', 'umidade']])
st.dataframe(df)
