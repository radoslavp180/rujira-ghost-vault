
let shares = if total_shares.is_zero() {
    amount
} else {
    amount.multiply_ratio(total_shares, total_assets)
};


if shares.is_zero() {
    return Err(ContractError::InvalidAmount { 
        msg: "Deposit too small to mint shares".to_string() 
    });
}




