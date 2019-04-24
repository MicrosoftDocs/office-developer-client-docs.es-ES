---
title: Acerca del registro de almacenes para la indización
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd2aa06a-96e8-1291-18b5-fc3c40b74e4d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 96322d12b3b7b334b5f78f81910dcf34c3fc78e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321829"
---
# <a name="about-registering-stores-for-indexing"></a>Acerca del registro de almacenes para la indización

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Este tema es específico de la búsqueda instantánea en Microsoft Office Outlook 2007.
  
La búsqueda instantánea le permite encontrar rápidamente elementos en Outlook. Usa componentes de la búsqueda en el escritorio de Windows.
  
El controlador de protocolo MAPI busca en el registro de Windows los almacenes que debe indizar para fines de búsqueda. Los proveedores de almacenamiento que deseen indizar deben registrarse en el registro de Windows.
  
De forma predeterminada, la búsqueda en el escritorio de Windows agrega los siguientes cuatro tipos de proveedores de almacenamiento al registro de Windows para permitir la indización:
  
- Almacén de archivos de carpetas personales (. PST).
    
-  Almacén de Microsoft Exchange, incluidos los archivos de carpetas sin conexión (. OST). 
    
-  Almacenar carpetas públicas. 
    
-  Tienda para Microsoft Office Outlook Connector para MSN. 
    
 Los proveedores de almacenamiento de terceros que deseen indizar deben registrarse en el registro de Windows. 
  
> [!NOTE]
> Los administradores y los usuarios pueden usar una configuración de directiva de grupo para impedir que la búsqueda en el escritorio de Windows no indexe los elementos de Outlook. Para obtener más información, consulte extender la búsqueda en el [escritorio de Windows](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx). 
  
## <a name="registry-keys"></a>Claves del registro

En un equipo, todos los proveedores de almacenamiento que deseen indizar deben registrarse solo en una de las tres claves del registro siguientes en el registro de Windows. El controlador de protocolo MAPI busca en cada una de estas claves en el orden siguiente:
  
1. [HKLM] \Software\Policies\Microsoft\Windows\Windows Search \
    
2. [HKLM] \Software\Microsoft\Windows\Windows Search\Preferences\
    
3. [HKCU] \Software\Microsoft\Windows\Windows Search\Preferences\
    
 Cada valor de la clave corresponde a un proveedor de almacenamiento que se indizaría. El nombre del valor es el identificador único global (GUID) del proveedor de almacenamiento, que es del tipo **DWORD** y tiene el valor hexadecimal 0x00000001. 
  
## <a name="guids-for-store-providers"></a>GUID para proveedores de almacenamiento

La propiedad MAPI **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** especifica el GUID de un almacén MAPI. En la siguiente tabla se describen los GUID para los proveedores de almacenamiento que los índices de Outlook. 
  
||||
|:-----|:-----|:-----|
|**Tipo de proveedor de almacén** <br/> |**GUID** <br/> |**Notas** <br/> |
|Archivos de carpetas personales (. ARCHIVOS  <br/> |{4154494E-BFF9-01B8-00AA-0037D96E0000}  <br/> |GUID se documenta en el archivo de encabezado público MSPST. h como **MSPST_UID_PROVIDER** <br/> |
|Exchange  <br/> |{C0A19454-7F29-1B10-A587-08002B2A2517}  <br/> |GUID se documenta en el archivo de encabezado público edkmdb. h como **pbExchangeProviderPrimaryUserGuid** <br/> |
|Carpetas públicas  <br/> |{70fab278-f7af-CD11-9bc8-00aa002fc45a}  <br/> |GUID se documenta en el archivo de encabezado público edkmdb. h como **pbExchangeProviderPublicGuid** <br/> |
|Outlook Connector para MSN  <br/> |{c34f5c97-EB05-bb4b-B199-2a7570ec7cf9}  <br/> |Ninguno  <br/> |
   
## <a name="see-also"></a>Vea también



[Información sobre la API del almacén](about-the-store-api.md)

