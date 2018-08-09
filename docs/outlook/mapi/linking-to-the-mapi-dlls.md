---
title: Vincular a las DLL de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19fd4678-21d3-47a6-a439-1d4959cac407
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 0bce1d682057b81135d1684c40bc79e6710d4e2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818019"
---
# <a name="linking-to-the-mapi-dlls"></a>Vincular a las DLL de MAPI

  
  
**Hace referencia a**: Outlook 
  
Los clientes MAPI pueden vincular a las DLL MAPI implícitamente o explícitamente mediante el uso de las funciones de Windows **LoadLibrary** y **GetProcAddress**. Para obtener información sobre la vinculación de forma explícita dll MAPI, vea el [vínculo a las funciones de MAPI](how-to-link-to-mapi-functions.md).
  
MAPI proporciona instrucciones de definición de tipo en el MAPIX. Archivo de encabezado de H para cada una de las siguientes funciones:
  
[MAPILogonEx](mapilogonex.md)
  
[MAPIUninitialize](mapiuninitialize.md)
  
[MAPIInitialize](mapiinitialize.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAdminProfiles](mapiadminprofiles.md)
  
Use estas definiciones de tipo para llamar correctamente a los puntos de entrada correspondiente si vincula explícitamente a la DLL de MAPI.
  
Proveedores de servicios pueden contener funcionalidad que no sean MAPI: las características que no están completamente relacionadas a MAPI: en su archivo DLL. Si necesita usar estas características, llame a **LoadLibrary** antes de usar el archivo DLL y **FreeLibrary** para quitar el archivo DLL de la memoria después de su uso. Debido a que no tiene constancia de usos de MAPI que no sean de un proveedor de servicios de DLL MAPI, no hay ninguna garantía de que el archivo DLL estará disponible cuando es necesario. MAPI libera un archivo DLL del proveedor de servicios cuando ya no hay ningún clientes con las sesiones activas que requieren sus servicios. 
  

