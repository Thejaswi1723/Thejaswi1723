module full_adder_structural(
    input a,
    input b,
    input cin,
    output sum,
    output cout
);
    wire w1, w2, w3;
    
    // XOR gates for sum
    xor (w1, a, b);
    xor (sum, w1, cin);
    
    // AND and OR gates for carry
    and (w2, a, b);
    and (w3, w1, cin);
    or (cout, w2, w3);
endmodule
