# python实现期权定价，期权交易策略（持续升级中....ing）
本项目致力于用python实现与期权定价，期权交易策略，波动率交易策略等代码。
# 期权定价
        import BSmodel as bs
        s,k,r,t,v,cp = 10,10,0.03,30/365,1
        """
        s:标的价格
        k:行权价格
        r:无风险利率
        t:剩余期限
        v:波动率
        cp:1为call ，-1为put
        """
        p1 = bs.caculateBSM(s,k,r,t,v,cp)
# 隐含波动率
        import BSmodel as bs
        s,k,r,t,v,cp = 10,10,0.03,30/365,1
        price = 1
        """
        price:期权市场价格
        s:标的价格
        k:行权价格
        r:无风险利率
        t:剩余期限
        cp:1为call ，-1为put
        """
        IV1 = bs.caculateIV_Newton(price,s,k,r,t,cp)# 牛顿法
        IV2 = bs.caculateIV_Dichotomy(price,s,k,r,t,cp) #二分法
