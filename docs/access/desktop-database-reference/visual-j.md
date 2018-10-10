---
title: Visual J ++ (referencia de escritorio de la base de datos de Access)
TOCTitle: Visual J++
ms:assetid: 5c05db85-cdf2-9a73-fbc5-3dbfa6752376
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249320(v=office.15)
ms:contentKeyID: 48545079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3bc76026fb5b5b426b41c8334bc61d5b9485dd76
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484952"
---
# <a name="visual-j"></a>Visual J++


**Se aplica a**: Access 2013 | Office 2013

En este breve ejemplo de Microsoft Visual J++, se muestra cómo puede asociar su propia función a un evento determinado.

```java 
 
// BeginEventExampleVJ 
import com.ms.wfc.data.*; 
 
public class EventExampleVJ 
{ 
 ConnectionEventHandler handler = new ConnectionEventHandler(this,"onConnectComplete"); 
 
 public void onConnectComplete(Object sender,ConnectionEvent e) 
 { 
 if (e.adStatus == AdoEnums.EventStatus.ERRORSOCCURRED) 
 System.out.println("Connection failed"); 
 else 
 System.out.println("Connection completed"); 
 return; 
 } 
 
 public static void main (String[] args) 
 { 
 EventExampleVJ Class1 = new EventExampleVJ(); 
 Connection conn = new Connection(); 
 
 conn.addOnConnectComplete(Class1.handler); // Enable event support. 
 conn.open("DSN=Pubs"); 
 conn.close(); 
 conn.removeOnConnectComplete(Class1.handler); // Disable event support. 
 } 
} 
// EndEventExampleVJ 
```

En primer lugar, el método de clase *onConnectionComplete* se asocia al evento **ConnectionComplete** mediante la creación de un nuevo objeto **ConnectionEventHandler** y la asignación de la función *onConnectComplete* al objeto.

A continuación, la función *principal* crea un objeto **Connection** y habilita el control llamando al método **addOnConnectComplete** y pasándole la dirección de la función de *controlador* de eventos.

