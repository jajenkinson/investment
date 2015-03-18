% tradeProfit
% John A. Jenkinson, UTSA ECE, SiViRT
% Tuesday March 18th, 2015
% The function calculates both the cost and the profit of a potential
% investment based on the number of shares involved in the transaction,
% the value of the shares at the time of buying and selling, and the 
% type of transaction being made ('m' for market, and 'l' for limit).
% The routing is assumed to be through NITE, which has a trading fee of
% $0.001 per share.  Fees are defined for transaction processed through 
% suretrader.com
% Suggestions for this code are welcomed at john.jenkinson@utsa.edu.
function[profit,cost]=tradeProfit(number_shares,buy_value,sell_value,...
    buy_type,sell_type)

    if (buy_type == 'm')
        buy = 5;
    elseif (buy_type == 'l')
        buy = 10;
    end
    
    if (sell_type == 'm')
        sell = 5;
    elseif (sell_type == 'l')
        sell = 10;
    end
    
    route = 0.001;
    routing_fee = 2*number_shares*route;
    invest = number_shares*buy_value;
    outvest = number_shares*sell_value;
    tax = 0.25*(outvest-invest);
    tithe = 0.1*(outvest-invest);
    
    cost = routing_fee + tax + tithe + buy + sell;
    profit = (outvest-invest)-cost;
    
end
