# calculate-VAT
def calculate_vat(net_amount, vat_rate):
    vat_amount = net_amount * vat_rate / 100
    gross_amount = net_amount + vat_amount
    return vat_amount, gross_amount

def extract_vat(gross_amount, vat_rate):
    vat_amount = gross_amount * vat_rate / (100 + vat_rate)
    net_amount = gross_amount - vat_amount
    return vat_amount, net_amount

# Example Usage
net_amount = 100
vat_rate = 20

vat_amount, gross_amount = calculate_vat(net_amount, vat_rate)
print(f"Net Amount: ${net_amount}, VAT Amount: ${vat_amount}, Gross Amount: ${gross_amount}")

gross_amount = 120

vat_amount, net_amount = extract_vat(gross_amount, vat_rate)
print(f"Gross Amount: ${gross_amount}, VAT Amount: ${vat_amount}, Net Amount: ${net_amount}")

