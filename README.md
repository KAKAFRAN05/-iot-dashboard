import pandas as pd
import streamlit as st
url = "LINK_CSV_AQUI"
df = pd.read_csv(url)
st.title("Monitoramento IoT")
st.line_chart(df[['temperatura', 'umidade']])
st.dataframe(df)
