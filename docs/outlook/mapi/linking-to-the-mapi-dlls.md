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
ms.openlocfilehash: 394537a60f4cb9603024115ccea67570291d8ac6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419306"
---
# <a name="linking-to-the-mapi-dlls"></a>Vincular a las DLL de MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los clientes MAPI pueden vincular a los ARCHIVOS DLL de MAPI de forma implícita o explícita mediante las funciones de Windows **LoadLibrary** y **GetProcAddress**. Para obtener información sobre la vinculación explícita de DLL de MAPI, vea [Vínculo a funciones MAPI](how-to-link-to-mapi-functions.md).
  
MAPI proporciona instrucciones de definición de tipo en MAPIX. Archivo de encabezado H para cada una de las siguientes funciones:
  
[MAPILogonEx](mapilogonex.md)
  
[MAPIUninitialize](mapiuninitialize.md)
  
[MAPIInitialize](mapiinitialize.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAdminProfiles](mapiadminprofiles.md)
  
Use estas definiciones de tipo para llamar correctamente a los puntos de entrada correspondientes si vincula explícitamente a los ARCHIVOS DLL de MAPI.
  
Los proveedores de servicios pueden contener funciones que no sean MAPI (características que no están completamente relacionadas con MAPI) en su DLL. Si necesitas usar estas características, llama **a LoadLibrary** antes de usar la DLL y **FreeLibrary** para quitar la DLL de la memoria después de su uso. Dado que MAPI no es consciente de los usos que no son MAPI de una DLL del proveedor de servicios, no hay ninguna garantía de que la DLL estará disponible cuando sea necesario. MAPI libera una DLL de proveedor de servicios cuando ya no hay clientes con sesiones activas que requieran sus servicios. 
  

