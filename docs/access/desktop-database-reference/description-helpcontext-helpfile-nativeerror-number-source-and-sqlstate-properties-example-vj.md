---
<<<<<<< Título HEAD: Description, ContextoDeAyuda (HelpContext), ejemplo de las propiedades HelpFile (VJ ++) TOCTitle: Description, ContextoDeAyuda (HelpContext), HelpFile, NativeError, número, origen y ejemplo de las propiedades SQLState (VJ ++) === título: descripción, ContextoDeAyuda (HelpContext), ejemplo de las propiedades HelpFile (VJ ++) TOCTitle: ejemplo de las propiedades Description, ContextoDeAyuda (HelpContext), HelpFile, NativeError, número, origen y SQLState (VJ ++)
>>>>>>> Master ms:assetid: daa3ff89-9f7f-f832-479e-bbb51c918ae8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250100(v=office.15) ms:contentKeyID: ms.date 48548085: 18/09/2015 mtps_version: Office.15
---

<<<<<<< HEAD
# <a name="description-helpcontext-helpfile-nativeerror-number-source-and-sqlstate-properties-example-vj"></a>Ejemplo de las propiedades Description, HelpContext, HelpFile, NativeError, Number, Source y SQLState (VJ++)
=======
# <a name="description-helpcontext-helpfile-nativeerror-number-source-and-sqlstate-properties-example-vj"></a>Ejemplo de las propiedades Description, ContextoDeAyuda (HelpContext), HelpFile, NativeError, número, origen y SQLState (VJ ++)
>>>>>>> master


**Se aplica a**: Access 2013 | Office 2013

Este ejemplo desencadena un error, lo captura y muestra las propiedades [Description](description-property-ado.md), [ContextoDeAyuda (HelpContext)](helpcontext-helpfile-properties-ado.md), [HelpFile](helpcontext-helpfile-properties-ado.md), [NativeError](nativeerror-property-ado.md), [Number](number-property-ado.md), [Source](source-property-ado-error.md) y [SQLState](sqlstate-property-ado.md) del objeto [Error](error-object-ado.md) resultante.

```java
    // BeginDescriptionJ
    // The WFC class includes the ADO objects.
    
    import com.ms.wfc.data.*;
    import java.io.* ;
    
    public class DescriptionX
    {
       // The main entry point for the application.
    
       public static void main (String[] args)
       {
          DescriptionX();
          System.exit(0);
       }
    
       // DescriptionX function
    
       static void DescriptionX()
       {
          // Declarations.
          BufferedReader in = new 
             BufferedReader(new InputStreamReader(System.in));
    
          // Define ADO Objects.
          Connection cnConn1 = null;
    
          try
          {
             // Intentionally trigger an error.
             cnConn1 = new Connection();
             cnConn1.open("nothing");
          }
          catch( AdoException ae )
          {
             // Notify user of any errors that result from ADO.
             PrintProviderError(cnConn1);
          }
    
          try
          {
             System.out.println("\nPress <Enter> key to continue.");
             in.readLine();
          }
          // System read requires this catch.
          catch( java.io.IOException je)
          {
             PrintIOError(je);
          }
      
       }
    
       // PrintProviderError Function
    
       static void PrintProviderError( Connection Cnn1 )
       {
          // Print Provider errors from Connection object.
          // ErrItem is an item object in the Connections Errors collection.
          com.ms.wfc.data.Error  ErrItem = null;
          long nCount = 0;
          int  i      = 0;
    
          nCount = Cnn1.getErrors().getCount();
    
          // If there are any errors in the collection, print them.
          if( nCount > 0);
          {
             // Collection ranges from 0 to nCount - 1
             for (i = 0; i< nCount; i++)
             {
                ErrItem = Cnn1.getErrors().getItem(i);
                System.out.println("\t Error number: " + ErrItem.getNumber()
                   + "\t" + ErrItem.getDescription() );
             }
          }
    
       }
    
       // PrintIOError Function
    
       static void PrintIOError( java.io.IOException je)
       {
          System.out.println("Error \n");
          System.out.println("\tSource = " + je.getClass() + "\n");
          System.out.println("\tDescription = " + je.getMessage() + "\n");
       }
    }
    // EndDescriptionJ
```
