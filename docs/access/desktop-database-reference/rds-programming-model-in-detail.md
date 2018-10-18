---
title: Modelo de programación detallado de RDS
TOCTitle: RDS Programming Model in Detail
ms:assetid: 133fc059-9b51-52e2-2e61-339716d8d965
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248906(v=office.15)
ms:contentKeyID: 48543364
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c68af31fec00178cf4f2a78cd64980ac0b262206
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604452"
---
# <a name="rds-programming-model-in-detail"></a>Modelo de programación detallado de RDS


**Se aplica a**: Access 2013 | Office 2013



A continuación se muestran los principales elementos del modelo de programación de RDS:

  - RDS. DataSpace

  - RDSServer.DataFactory

  - RDS. DataControl

  - Evento

## <a name="rdsdataspace"></a>RDS. DataSpace

La aplicación de cliente debe especificar el servidor y el programa de servidor que se van a invocar. A cambio, la aplicación recibe una referencia al programa de servidor y puede tratar la referencia como si fuese el propio programa de servidor.

El modelo de objetos de RDS incluye esta funcionalidad con el objeto [RDS.DataSpace](dataspace-object-rds.md).

El programa de servidor se especifica con un identificador de programa o *ProgID*. El servidor utiliza el *ProgID* y el Registro del equipo servidor para buscar información sobre el programa real que debe iniciar.

RDS hace una distinción interna dependiendo de si el programa de servidor está ubicado en un servidor remoto en Internet o en una intranet, en un servidor de una red local o no está en ningún servidor sino en una biblioteca de vínculos dinámicos (DLL) local. Esta distinción determina cómo se intercambia la información entre el cliente y el servidor, y afecta de manera tangible al tipo de referencia devuelto a la aplicación de cliente. Sin embargo, desde el punto de vista del usuario, esta distinción no tiene ningún significado especial. Lo más importante es que reciba una referencia de programa utilizable.

## <a name="rdsserverdatafactory"></a>RDSServer.DataFactory

RDS proporciona un programa de servidor predeterminado que puede realizar una consulta SQL en el origen de datos y devolver un objeto [Recordset](recordset-object-ado.md) o tomar un objeto **Recordset** y actualizar el origen de datos.

El modelo de objetos de RDS incluye esta funcionalidad con el objeto [RDSServer.DataFactory](datafactory-object-rdsserver.md).

<<<<<<< Además de en el encabezado, este objeto tiene un método para la creación de un objeto **Recordset** vacío que se puede rellenar mediante programación ([CreateRecordset](createrecordset-method-rds.md)) y otro método para convertir un objeto **Recordset** en un texto cadena que se va a crear una página Web ([ConvertToString](converttostring-method-rds.md)).
=== Además, este objeto tiene un método para la creación de un objeto **Recordset** vacío que se puede rellenar mediante programación ([CreateRecordset](createrecordset-method-rds.md)) y otro método para convertir un objeto **Recordset** en una cadena de texto para crear una página Web () [ConvertToString](converttostring-method-rds.md)).
>>>>>>> master

Con ADO, se pueden invalidar algunos de los comportamientos estándar de conexión y comandos de **RDSServer.DataFactory** con un controlador **DataFactory** y un archivo de personalización que contiene parámetros de conexión, comando y seguridad.

El programa de servidor se denomina a veces *objeto de negocio*. Se puede escribir un objeto de negocio personalizado que pueda realizar operaciones complicadas de acceso, comprobación de validez, etc. Incluso cuando se escribe un objeto de negocio personalizado, se puede crear una instancia de un objeto **RDSServer.DataFactory** y utilizar algunos de sus métodos para llevar a cabo las tareas.

## <a name="rdsdatacontrol"></a>RDS. DataControl

RDS permite combinar la funcionalidad de **RDS.DataSpace** y **RDSServer.DataFactory**, además de permitir a los controles visuales usar fácilmente el objeto **Recordset** devuelto por una consulta de un origen de datos. Normalmente, RDS intenta obtener automáticamente acceso a la información ubicada en un servidor y mostrarla en un control visual.

El modelo de objetos de RDS incluye esta funcionalidad con el objeto [RDS.DataControl](datacontrol-object-rds.md).

**RDS.DataControl** tiene dos aspectos. Un aspecto pertenece al origen de datos. Si se configura el comando y la información de conexión mediante las propiedades **Connect** y **SQL** de **RDS.DataControl**, usará automáticamente **RDS.DataSpace** para crear una referencia al objeto **RDSServer.DataFactory** predeterminado. A continuación, **RDSServer.DataFactory** usará el valor de la propiedad **Connect** para conectarse al origen de datos, usará el valor de la propiedad **SQL** para obtener un objeto **Recordset** del origen de datos y devolverá el objeto **Recordset** a **RDS.DataControl**.

<<<<<<< HEAD el segundo aspecto pertenece a la presentación de devuelve información del **conjunto de registros** en un control visual. Se puede asociar un control visual al objeto **RDS.DataControl** (en un proceso, se denomina enlace) y obtener acceso a la información del objeto **Recordset** asociado, que muestra los resultados de consulta en una página Web en Microsoft® Internet Explorer. Cada objeto **RDS.DataControl** enlaza un objeto **Recordset**, que representa los resultados de una consulta única, a uno o varios controles visuales (por ejemplo, un cuadro de texto, un cuadro combinado, un control de cuadrícula, etc.). Puede haber más de un objeto **RDS.DataControl** en cada página. Cada objeto **RDS.DataControl** puede conectarse con un origen de datos diferente y contiene los resultados de una consulta independiente.
=== El segundo aspecto pertenece a la presentación de la información devuelta de **Recordset** en un control visual. Puede asociar un control visual con el **RDS. DataControl** (en un proceso que se denomina enlace) y obtener acceso a la información en el objeto **Recordset** asociado, mostrar resultados de la consulta en una página Web en Microsoft® Internet Explorer. Cada objeto **RDS.DataControl** enlaza un objeto **Recordset**, que representa los resultados de una consulta única, a uno o varios controles visuales (por ejemplo, un cuadro de texto, un cuadro combinado, un control de cuadrícula, etc.). Puede haber más de un objeto **RDS.DataControl** en cada página. Cada objeto **RDS.DataControl** puede conectarse con un origen de datos diferente y contiene los resultados de una consulta independiente.
>>>>>>> master

El objeto **RDS.DataControl** también tiene sus propios métodos para explorar, ordenar y filtrar las filas del objeto **Recordset** asociado. Estos métodos son similares pero no iguales a los métodos del objeto **Recordset** de ADO.

## <a name="events"></a>Eventos

RDS admite dos de sus propios eventos, que son independientes del modelo de eventos de ADO. El evento [onreadystatechange recibe una](onreadystatechange-event-rds.md) llamada siempre que el **RDS. DataControl** propiedad [ReadyState](readystate-property-rds.md) cambia, por lo que notifica cuando una operación asincrónica ha finalizado correctamente, terminada, o se produjo un error. El evento [onError](onerror-event-rds.md) se invoca cada vez que se genera un error, incluso si se produce durante una operación asincrónica.


> [!NOTE]
> <P>[!NOTA] Microsoft Internet Explorer proporciona a RDS dos eventos adicionales: <STRONG>ondatasetchanged</STRONG> (el objeto <STRONG>Recordset</STRONG> es funcional pero sigue recuperando filas) y <STRONG>ondatasetcomplete</STRONG> (el objeto <STRONG>Recordset</STRONG> dejó de recuperar filas).</P>


