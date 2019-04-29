---
title: Las carpetas de recepci�n de MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2e1287a3-0f15-4d9a-b7ee-738fce9cd51f
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: b22b8641d55037d3755fc9ae32b97455223bbd12
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431942"
---
# <a name="mapi-receive-folders"></a>Las carpetas de recepci�n de MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una carpeta de recepci�n contiene los mensajes entrantes de una clase de mensaje en particular. Recibir carpeta asociaciones pueden establecerse por los clientes, el proveedor de almacenamiento de mensajes o MAPI. MAPI tiene dos predeterminada las carpetas de recepci�n: la carpeta ra�z del almac�n de mensajes y a continuaci�n, la carpeta Bandeja de entrada del sub�rbol de mensajes interpersonales (IPM). La carpeta ra�z del almac�n de mensajes es el valor predeterminado recibir carpeta para todos los mensajes de comunicaci�n entre procesos (IPC).
  
 La carpeta Bandeja de entrada se crea mediante MAPI para cada nuevo almac�n de mensajes y act�a como el valor predeterminado recibe carpeta para las siguientes clases de mensaje: 
  
- La clase de mensaje IPM.
    
- La clase de mensaje de informe.
    
- Una clase vac�a o que faltan.
    
Todos los mensajes de informe, incluso los que se env�a en respuesta a un mensaje de IPC, se colocan en la carpeta Bandeja de entrada. Las aplicaciones de cliente IPC que procesan sus propios informes expl�citamente deben agregar una carpeta de recepci�n para la clase espec�fica del informe. Por ejemplo, si un cliente espera recibir los mensajes con la clase IPC. Paper.Order, debe llamar al m�todo de [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) para establecer una carpeta de recepci�n de informes con la clase Report.IPC.Paper.Order. 
  
Recibir carpeta de asociaciones se basan en la organizaci�n jer�rquica de las clases de mensajes. Los clientes pueden establecer una asociaci�n entre una carpeta de recepci�n y una clase de mensaje o utilizar las carpetas de recepci�n predeterminado MAPI de forma expl�cita. Normalmente, los clientes de designaci�n una carpeta para recibir los mensajes de una clase base y todas sus subclases. Por ejemplo, un cliente t�pico ser�a establecer una asociaci�n para los mensajes con la clase **MyClass**. A continuaci�n, si el cliente recibe los mensajes con clases **MyClass.Home** o **MyClass.Home.Kitchen.Computer**, estos mensajes se vaya a la carpeta de recepci�n de la clase base, **MyClass**.
  
Hay tres mensaje m�todos de almacenamiento que utilizan los clientes para trabajar con las carpetas de recepci�n:
  
- [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md)
    
- [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)
    
- [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md)
    
En la tabla de la carpeta de recepci�n es una lista de informaci�n acerca de todas las carpetas de recepci�n establecidas para un almac�n de mensajes. Su conjunto de columna necesaria incluye la clase de mensaje, la clave de registro y el identificador de entrada.
  
To retrieve a receive folder for a particular message class, clients pass the message class string to the [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) method. The message store provider returns an entry identifier for the corresponding folder. To implement **GetReceiveFolder**, a message store provider should use an algorithm that selects the folder whose associated message class matches the longest possible prefix of the specified message class. For example, assume the message store has the following associations between receive folders and message classes in its receive folder table:
  
- los mensajes de **IPM** se colocan en la carpeta Bandeja de entrada. 
    
- los mensajes de **IPM.Note.Sample** se colocan en la carpeta ejemplos. 
    
La siguiente tabla se muestra c�mo se enrutan los mensajes con varias clases a la correspondiente carpeta de recepci�n.
  
|**Clase de mensaje entrante**|**Carpeta de recepci�n**|
|:-----|:-----|
|**IPM. Note. sample. simple** <br/> |Carpeta de ejemplos  <br/> |
|**IPM.Note** <br/> |Carpeta Bandeja de entrada  <br/> |
|**IPM. Electrónicas** <br/> |Carpeta Bandeja de entrada  <br/> |
|**IPM. Note. sample. simple.** <br/> |Carpeta de ejemplos  <br/> |
   
Los clientes de llaman al m�todo de **SetReceiveFolder** para realizar una asociaci�n expl�cita entre una clase de mensaje concreto y recibir carpeta. Cuando un mensaje se entrega a una clase de mensaje vac�a, MAPI coloca el mensaje en la carpeta de recepci�n que se define para un prefijo de la clase vac�a. Por ejemplo, si el cliente tiene una carpeta de recepci�n establecida para los mensajes con la clase **IPM** y se env�a un mensaje con la clase **IPM.Note.Test**, este mensaje se colocar� en la carpeta de recepci�n para la clase de mensaje **IPM**. 
  
Al llamar a **SetReceiveFolder**, los clientes suelen pasan una cadena de la clase de mensaje y el identificador de entrada de la nueva carpeta de recepci�n. Sin embargo, los clientes pueden pasar en NULL para uno o ambos de estos par�metros. En la siguiente tabla describe el comportamiento resultante de la especificaci�n de NULL para los par�metros de identificador de entrada y la clase de mensaje. 
  
|**par�metro  _SetReceiveFolder_**|**Comportamiento resultante**|
|:-----|:-----|
|Identificador de entrada que se establece en NULL  <br/> |El almac�n de mensajes elimina la asociaci�n entre especificado clase y sus existentes de la carpeta de recepci�n de mensajes. Recibir una nueva carpeta no se ha establecido. <br/> Las llamadas subsiguientes a **GetReceiveFolder** con esta clase de mensaje devolver� la carpeta de recepci�n para un prefijo de la clase de mensaje. para los almacenes de mensajes nuevos, **GetReceiveFolder** devolver� la Bandeja de entrada en el sub�rbol IPM.      <br/> |
|Clase de mensaje que se establece en NULL  <br/> |El almac�n de mensajes, cambia la asociaci�n de la clase de mensaje vac�a en la carpeta indicada. Los mensajes entrantes en caso contrario, se reconoce cuya clase se vaya a esta carpeta.  <br/> |
|Identificador de entrada y la clase de mensaje se establecen en NULL  <br/> |El almac�n de mensajes, elimina la asociaci�n de clase o carpeta para la clase de mensaje vac�o. No deben establecer ambos par�metros en NULL, porque normalmente resulta en los mensajes entrantes que se coloca en la carpeta ra�z del almac�n de mensajes, una carpeta que no es visible para el cliente.  <br/> |
   
Aunque la clase de un mensaje nunca debe estar vac�o, se puede producir una clase de mensaje vac�a. Es responsabilidad del almac�n de mensajes para asignar la clase de mensaje a **IPM** para nuevos mensajes salientes que tienen una clase vac�a; es responsabilidad del proveedor de transporte para asignar **IPM.Note** como la clase para los mensajes entrantes que tienen cualquier clase vac�a. 
  
## <a name="see-also"></a>Ver también



[Carpetas de MAPI](mapi-folders.md)

