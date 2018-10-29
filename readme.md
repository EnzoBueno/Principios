# Ejercicios de DIP, ISP, SRP
## Ejercicio 1 

**DIP:** La clase AnalizadorDatos depende de BaseDeDatos, la cual es menos abstracta.

**ISP:** Si cumple

**SRP:** La clase DataBaseObject cumple con el principio, pero las demas no.
La clase BasedeDatos tiene demasiadas responsabilidades (razones de cambio), si el objeto cambia de formato
la clase tenfria que cambiar, y si el objeto cambia su contenido tambien habria que cambiar la clase.
La clase AnalizadorDatos tambien es fragil, si queremos cambiar la condicion, o el mensaje, o la forma de 
analizar el objeto habria que cambiar la clase.


## Ejercicio 2

```cs
using System;

//Objeto que representa un dato de la base de datos.
class DataBaseObject
{
    public string Descripcion { get; }
}

//Base de datos.
class BaseDeDatos
{
    public DataBaseObject ObtenerDato(string clave)
    {
        //Devuelve el dato correspondiente a la clave
    }
    public void GrabarDato(string clave, DataBaseObject dato)
    {
        //Graba el dato en la base de datos, bajo la clave dada
    }
    public String[] ListarClaves()
    {
        //Devuelve un String[] con todas las claves
    }
    public String[] ListarDescripcionDatos()
    {
        //Devuelve un String[] con la descripción de todas los 
        //datos almacenados en  la base
    }
    public DataBaseObject[] ListarDatos()
    {
        //Devuelve un DataBaseObject[] con todos los datos almacenados en la base
    }
}
class AnlizadorDatos
{
    private BaseDeDatos baseDatos{get; set;};
    public void Analizar()
    {
        foreach (DataBaseObject DBObj in baseDatos.ListarDatos())
        {
            if (CumpleCondicion(DBObj))
            {
                MensajeUno();
            }
            else
            {
                MensajeDos();
            }
        }
    }
}
class Condicion
{
    public bool Cumplecondicion(DataBaseObject DBobj)
    {
        //Devuelve true si se cumple una cierta condición
    }
    public void MensajeUno()
    { /*Mensaje predeterminado*/ }
    public void MensajeDos()
    { /*Mensaje predeterminado*/ }
}
```
## Ejercicio 3 

```cs
////Insertar el código corregido. El ejercicio 2 y 3 pueden ser resueltos de forma conjunta

```