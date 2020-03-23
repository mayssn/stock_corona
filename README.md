# stock_corona



sp = read_csv(
    '~/Desktop/Corona/S&P500.csv', delimiter=r",")
sp= sp[['Date', 'Close','Volume']]
print(sp)

cd = read_csv(
    '~/Desktop/Corona/COVID19.csv', delimiter=r",")
cd = cd.rename(columns={"DateRep": "Date", "Countries and territories": "Country"}, errors="raise")
cd= cd[['Date', 'Cases','Deaths','Country']]

pd.to_datetime(cd['Date'])

print(cd.dtypes)

print(cd)
print(sp)

mayssn@gmail.com
