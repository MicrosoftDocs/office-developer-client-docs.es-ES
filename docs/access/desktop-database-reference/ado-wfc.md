---
title: ADO para Windows Foundation Classes (ADO/WFC)
TOCTitle: ADO/WFC
ms:assetid: 73206be8-6515-79e4-e904-cc2d0d59411d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249468(v=office.15)
ms:contentKeyID: 48545628
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fd5b54160bfa6c692bfcd6489646021dcce34631
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485136"
---
# <a name="adowfc"></a>ADO/WFC


**Se aplica a**: Access 2013 | Office 2013

ADO para Windows Foundation Classes (ADO/WFC) se basa en el modelo de eventos de ADO y presenta una interfaz de programación de aplicaciones simplificada. En general, ADO/WFC intercepta eventos de ADO, consolida los parámetros de eventos en una sola clase de eventos y, a continuación, llama al controlador de eventos.

**Para utilizar eventos de ADO en ADO/WFC**

1.  Defina su propio controlador de eventos para procesar un evento. Por ejemplo, para procesar el evento **ConnectComplete** de la familia **ConnectionEvent**, podría utilizar este código:
    
    ```java 
     
    public void onConnectComplete(Object sender,ConnectionEvent e) 
    { 
        System.out.println("onConnectComplete:" + e); 
    } 
    ```

2.  Defina un objeto handler que represente su controlador de eventos. El objeto handler debe ser de tipo de datos **ConnectEventHandler** para un evento de tipo **ConnectionEvent**, o de tipo de datos **RecordsetEventHandler** para un evento de tipo **RecordsetEvent**. Por ejemplo, cree el siguiente código para su controlador de eventos **ConnectComplete**:
    
    ```java
        ConnectionEventHandler handler =  
                new ConnectionEventHandler(this, "onConnectComplete"); 
    ```

    El primer argumento del constructor **ConnectionEventHandler** es una referencia a la clase que contiene el controlador de eventos que se menciona en el segundo argumento. El compilador de Microsoft Visual J++ también admite una sintaxis equivalente:
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this, "onConnectComplete"); 
    ```
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this.onConnectComplete); 
    ```
    
    El primer argumento del constructor **ConnectionEventHandler** es una referencia a la clase que contiene el controlador de eventos que se menciona en el segundo argumento. El compilador de Microsoft Visual J++ también admite una sintaxis equivalente:
    
    ```java 
     
        ConnectionEventHandler handler =  
            new ConnectionEventHandler(this.onConnectComplete); 
    ```
    
    

El único argumento es una referencia a la clase (**this**) y al método deseados dentro de la clase (**onConnectComplete**).


3.  Agregue su controlador de eventos a una lista de controladores designados para procesar un tipo determinado de evento. Utilice el método con un nombre como **addOn *** EventName*(*controlador*).

4.  ADO/WFC implementa internamente todos los controladores de eventos de ADO. Por tanto, un evento causado por una operación **Connection** o **Recordset** es interceptado por un controlador de eventos de ADO/WFC. El controlador de eventos de ADO/WFC pasa parámetros **ConnectionEvent** de ADO en una instancia de la clase **ConnectionEvent** de ADO/WFC, o parámetros **RecordsetEvent** de ADO en una instancia de la clase **RecordsetEvent** de ADO/WFC. Estas clases de ADO/WFC consolidan los parámetros de eventos de ADO; es decir, que cada clase de ADO/WFC contiene un elemento de datos para cada parámetro único en todos los métodos **ConnectionEvent** o **RecordsetEvent** de ADO.

5.  Después, ADO/WFC llama al controlador de eventos con el objeto event de ADO/WFC. Por ejemplo, el controlador **onConnectComplete** tiene una firma similar a:
    
    ```java 
     
        public void onConnectComplete(Object sender,ConnectionEvent e) 
    ```
    
    El primer argumento es el tipo de objeto que envió el evento ([Connection](connection-object-ado.md) o [Recordset](recordset-object-ado.md)) y el segundo argumento es el objeto event de ADO/WFC (**ConnectionEvent** o **RecordsetEvent**). La firma del controlador de eventos es más sencilla que un evento de ADO. Sin embargo, es necesario que comprenda el modelo de eventos de ADO para saber qué parámetros son aplicables a un evento y cómo responder.

6.  Vuelva desde el controlador de eventos al controlador de ADO/WFC correspondiente al evento de ADO. ADO/WFC copia elementos de datos de eventos de ADO/WFC pertinentes de nuevo en los parámetros de eventos de ADO y, a continuación, vuelve el controlador de eventos de ADO.

7.  Cuando haya finalizado el procesamiento, quite su controlador de la lista de controladores de eventos de ADO/WFC. Utilice el método con un nombre como **removeOn *** EventName*(*controlador*).

