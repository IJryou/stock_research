# #1. 주가데이터 수집

- 주가데이터 수집은 가장 간편한 방법인 pandas-datareader를 활용함

    import pandas_datareader as pdr
    import datetime as dt
    
    # data를 얻어오는 객체 선언
    web = pdr.data
    
    start, end = dt.datetime(1920, 1, 1), dt.datetime(2013, 12, 31)
    
    # data to pandas data frame
    web.DataReader('IBM','yahoo', start, end).reset_index()