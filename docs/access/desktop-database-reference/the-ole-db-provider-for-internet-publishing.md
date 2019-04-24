---
title: OLE DB Provider for Internet Publishing
TOCTitle: The OLE DB Provider for Internet Publishing
ms:assetid: 864e5ece-0f50-5d88-4c40-f951b2a2eded
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249583(v=office.15)
ms:contentKeyID: 48546082
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 617dca5ced5410e2023657ea1b0b748066f7843f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314059"
---
# <a name="ole-db-provider-for-internet-publishing"></a>Proveedor OLE DB para la publicación en Internet

**Se aplica a:** Access 2013, Office 2013

Los objetos [Record](record-object-ado.md) y [Stream](stream-object-ado.md) de ADO se pueden usar con Microsoft OLE DB Provider for Internet Publishing (Internet Publishing Provider) para tener acceso a recursos, como carpetas web o archivos atendidos por Microsoft FrontPage, y manipularlos. Con ADO, puede especificar que el origen de un **Record**, de un **Stream** o de un [Recordset](recordset-object-ado.md) sea una dirección URL. Después, puede cargar, descargar, mover, copiar y eliminar recursos, o manipular directamente las propiedades de los recursos.

Para obtener un ejemplo de código que utiliza **Records** y **Streams** con el Proveedor de publicación en Internet, vea el [Escenario de Internet Publishing](internet-publishing-scenario.md).

El Proveedor de publicación en Internet se instala con Microsoft Windows 2000. También existen versiones anteriores del proveedor disponibles con Microsoft Office 2000 y Microsoft Internet Explorer 5.0.

Hay tres maneras de conectar ADO con el Proveedor de publicación en Internet:

- Especifique "URL=" en la cadena de conexión. Por ejemplo:
    
  ```vb 
     
    objConn.Open "URL=https://servername" 
  ```

- Especifique Msdaipp.dso para la palabra clave *Provider* de la cadena de conexión. Por ejemplo:
    
  ```vb 
     
    objConn.Open "provider=MSDAIPP.DSO;data source=https://servername" 
  ```

- Especifique Msdaipp.dso para la propiedad [Provider](provider-property-ado.md) del objeto [Connection](connection-object-ado.md). Por ejemplo:
    
  ```vb 
     
    objConn.Provider = "MSDAIPP.DSO" 
    objConn.Open "https://servername" 
  ```

> [!NOTE]
> Si se especifica explícitamente Msdaipp.dso como valor del proveedor, ya sea con la palabra clave *Provider* de la cadena de conexión o con la propiedad **Provider**, no podrá utilizar "URL=" en la cadena de conexión. Si lo hace, se producirá un error. En su lugar, simplemente especifique la dirección URL tal y como se muestra anteriormente en este tema.

Para obtener información más específica acerca del proveedor de publicación en Internet, vea [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) o la documentación del proveedor proporcionada con la aplicación de origen con la que se instaló: Windows 2000, Office 2000 o Internet Explorer 5.0.

