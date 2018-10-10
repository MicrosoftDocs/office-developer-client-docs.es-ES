---
title: OLE DB Provider for Internet Publishing
TOCTitle: The OLE DB Provider for Internet Publishing
ms:assetid: 864e5ece-0f50-5d88-4c40-f951b2a2eded
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249583(v=office.15)
ms:contentKeyID: 48546082
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f9f8fbed638c07e55b3ecb1730633dceee2b5c7e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483722"
---
# <a name="the-ole-db-provider-for-internet-publishing"></a>OLE DB Provider for Internet Publishing


**Se aplica a**: Access 2013 | Office 2013

Los objetos [Record](record-object-ado.md) y [Stream](stream-object-ado.md) de ADO se pueden usar con Microsoft OLE DB Provider for Internet Publishing para obtener acceso a recursos, tales como carpetas Web o archivos, proporcionados por Microsoft FrontPage y manipularlos. Con ADO, puede especificar que el origen de un **Record**, de un **Stream** o de un [Recordset](recordset-object-ado.md) sea una dirección URL. Después, puede cargar, descargar, mover, copiar y eliminar recursos, o manipular directamente las propiedades de los recursos.

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
> <P>Si se especifica explícitamente Msdaipp.dso como valor del proveedor, ya sea con la palabra clave la cadena de conexión de <EM>proveedor</EM> o la propiedad <STRONG>Provider</STRONG> , no se puede usar "dirección URL =" en la cadena de conexión. Si lo hace, se producirá un error. En su lugar, especifique simplemente la dirección URL como se muestra arriba.</P>



Para obtener información más específica acerca del proveedor de publicación en Internet, vea [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) o la documentación del proveedor proporcionada con la aplicación de origen con la que se instaló: Windows 2000, Office 2000 o Internet Explorer 5.0.

