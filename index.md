# Hi, this is an H1 header in markdown 
## Hi, this is an H2 header in markdown
### Hi, this is an H3 header in markdown
I have added three different headers using markdown.

## Now, I´m going to add and image 

![Image of DNA molecule](https://cdn-ikpklcn.nitrocdn.com/empcKXWCMaOlfGnEfQUllGEejyvrEPbB/assets/images/optimized/rev-ff8193a/adntro.com/wp-content/uploads/2023/02/image-3.png)

## Now it's time to add some python code 

``` python
def calibration_curve(model, x_val, y_val):

    from sklearn.calibration import calibration_curve
    
    # Ahora normalized_probs está en el rango [0, 1]
    
    # Obtener probabilidades predichas y aplanar ambos arrays
    y_pred_probs = model.predict(X_val).flatten()
    y_val_flattened = y_val.flatten()  # Aplanar y_val
    
    # Calcular la curva de calibración
    prob_true, prob_pred = calibration_curve(y_val_flattened, y_pred_probs, n_bins=20)
    
    # Graficar la curva de calibración
    plt.plot(prob_pred, prob_true, marker='o', label='Modelo')
    plt.plot([0, 1], [0, 1], linestyle='--', label='Perfectamente calibrado')
    plt.xlabel('Probabilidad predicha')
    plt.ylabel('Fraccion de positivos')
    plt.legend()
    plt.show()
```
