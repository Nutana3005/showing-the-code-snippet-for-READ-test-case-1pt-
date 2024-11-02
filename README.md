# showing-the-code-snippet-for-READ-test-case-1pt-
def test_read_product(self):
    # Add a sample product
    product = Product(name="ReadTestProduct", category="CategoryX", available=True)
    product.save()
    
    # Send a GET request to read the product
    response = self.client.get(f"/products/{product.id}")
    
    # Assert that the response contains the correct product details
    assert response.status_code == 200
    assert response.json['name'] == "ReadTestProduct"
