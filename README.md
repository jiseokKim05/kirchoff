# kirchoff

A = [8 3; 6 -3]; 
B = [30; 0];     
I = A \ B;        
i1 = I(1);
i2 = I(2);
i3 = i2 - i1;     
disp(['i1 = ', num2str(i1), ' A']);
disp(['i2 = ', num2str(i2), ' A']);
disp(['i3 = ', num2str(i3), ' A']);



A = [-2 1; 1 -11];  
B = [-5; -10];      
I = A \ B;          
i1 = I(1);
i2 = I(2);
disp(['i1 = ', num2str(i1), ' A']);
disp(['i2 = ', num2str(i2), ' A']);



A = [140 -30 0; -30 120 -50; 0 -50 100]; 
B = [120; 60; -270];  
I = A \ B; 
i1 = I(1);
i2 = I(2);
i3 = I(3);
disp(['i1 = ', num2str(i1), ' A']);
disp(['i2 = ', num2str(i2), ' A']);
disp(['i3 = ', num2str(i3), ' A']);



R1 = 30;
R2 = 40;
R3 = 90;
RL = 20;
Vs1 = 120;
Vs2 = 60;
Vs3 = 270;

A = [R1+RL, -R1, 0; 
    -R1, R1+R2, -R2;
    0, -R2, R2+R3];
B = [Vs1; Vs2; Vs3];

I = A \ B; 

disp('루프 전류 값 (A):');
disp(I);



V1 = 12;  
V2 = 9;    
I = 3; 
R1 = 3; 
R2 = 6;     
R3 = 4;    

A = [1, -1/R1, 0;
     -1/R1, 1/R1 + 1/R2, 0;
     0, 0, 1];
     
b = [I; V1/R2; V2];

V = A\b;

fprintf('Va = %.2f V\n', V(1));
fprintf('Vb = %.2f V\n', V(2));
fprintf('Vc = %.2f V\n', V(3));




E1 = 12;
E2 = 8;
R1 = 3;
R2 = 2;
R3 = 2; 
A = [R1+R2, -R2;
     -R2, R2+R3];     
b = [E1; E2];
I = A\b;
I1 = I(1); 
I2 = I(2);
I3 = I1 - I2;
V_R1 = I1 * R1;
V_R2 = I3 * R2;
V_R3 = I2 * R3;
P_R1 = I1^2 * R1;
P_R2 = I3^2 * R2;
P_R3 = I2^2 * R3;
P_E1 = E1 * I1;
P_E2 = E2 * I2;
fprintf('Currents:\n');
fprintf('I1 = %.2f A\n', I1);
fprintf('I2 = %.2f A\n', I2);
fprintf('I3 = %.2f A\n\n', I3);
