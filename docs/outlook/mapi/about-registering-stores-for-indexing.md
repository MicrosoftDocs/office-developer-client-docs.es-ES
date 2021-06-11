---
title: Acerca del registro de almacenes para indización
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
# <a name="about-registering-stores-for-indexing"></a>Acerca del registro de almacenes para indización

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Este tema es específico de la búsqueda instantánea en Microsoft Office Outlook 2007.
  
La búsqueda instantánea le permite buscar rápidamente elementos en Outlook. Usa componentes de Windows búsqueda de escritorio.
  
El controlador de protocolo MAPI comprueba Windows registro de almacenes que debe indizar con fines de búsqueda. Los proveedores de almacenamiento que desean indizarse deben estar registrados en el Windows registro.
  
De forma predeterminada, Windows búsqueda de escritorio agrega los siguientes cuatro tipos de proveedores de almacenamiento al registro de Windows para permitir la indización:
  
- Almacenar archivos de carpetas personales (. PST).
    
-  Microsoft Exchange, incluidos los archivos de carpeta sin conexión (.ost). 
    
-  Almacenar para carpetas públicas. 
    
-  Almacenar para Microsoft Office Outlook Connector para MSN. 
    
 Los proveedores de almacenes de terceros que desean indizarse deben registrarse en el registro Windows usuario. 
  
> [!NOTE]
> Los administradores y usuarios pueden usar una configuración de directiva de grupo para evitar que Windows búsqueda de escritorio indexe Outlook elementos. Para obtener más información, vea [Extending Windows Desktop Search](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx). 
  
## <a name="registry-keys"></a>Claves del Registro

En un equipo, todos los proveedores de almacén que quieran indizarse deben registrarse solo en una de las tres claves del Registro siguientes en Windows registro. El controlador de protocolo MAPI busca debajo de cada una de estas claves en el orden siguiente:
  
1. [HKLM]\Software\Policies\Microsoft\Windows\Windows Search\
    
2. [HKLM]\Software\Microsoft\Windows\Windows Search\Preferences\
    
3. [HKCU]\Software\Microsoft\Windows\Windows Search\Preferences\
    
 Cada valor bajo la clave corresponde a un proveedor de almacén que se indizaría. El nombre del valor es el identificador único global (GUID) del proveedor de almacén, que es del tipo **DWORD** y tiene el valor hexadecimal 0x00000001. 
  
## <a name="guids-for-store-providers"></a>GUID para proveedores de tienda

La propiedad MAPI **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** especifica el GUID de un almacén MAPI. En la tabla siguiente se describen los GUID para los proveedores de Outlook los índices de almacenamiento. 
  
||||
|:-----|:-----|:-----|
|**Tipo de proveedor de la tienda** <br/> |**GUID** <br/> |**Notas** <br/> |
|Archivos de carpetas personales (. PST)  <br/> |{4154494E-BFF9-01B8-00AA-0037D96E0000}  <br/> |GUID se documenta en el archivo de encabezado público mspst.h como **MSPST_UID_PROVIDER** <br/> |
|Exchange  <br/> |{C0A19454-7F29-1B10-A587-08002B2A2517}  <br/> |GUID se documenta en el archivo de encabezado público edkmdb.h como **pbExchangeProviderPrimaryUserGuid** <br/> |
|Carpetas públicas  <br/> |{70fab278-f7af-cd11-9bc8-00aa002fc45a}  <br/> |GUID se documenta en el archivo de encabezado público edkmdb.h como **pbExchangeProviderPublicGuid** <br/> |
|Outlook Conector para MSN  <br/> |{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}  <br/> |Ninguno  <br/> |
   
## <a name="see-also"></a>Vea también



[Información sobre la API del almacén](about-the-store-api.md)

