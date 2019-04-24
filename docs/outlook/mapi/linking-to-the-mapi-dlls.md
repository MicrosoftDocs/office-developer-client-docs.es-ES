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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270045"
---
# <a name="linking-to-the-mapi-dlls"></a>Vincular a las DLL de MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Los clientes MAPI se pueden vincular a las dll de MAPI implícita o explícitamente mediante las funciones de Windows **LoadLibrary** y **GetProcAddress**. Para obtener información sobre cómo vincular explícitamente dll MAPI, vea [Link to MAPI Functions](how-to-link-to-mapi-functions.md).
  
MAPI proporciona instrucciones de definición de tipo en MAPIX. H para cada una de las siguientes funciones:
  
[MAPILogonEx](mapilogonex.md)
  
[MAPIUninitialize](mapiuninitialize.md)
  
[MAPIInitialize](mapiinitialize.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAdminProfiles](mapiadminprofiles.md)
  
Use estas definiciones de tipo para llamar correctamente a los puntos de entrada correspondientes si tiene un vínculo explícito a los archivos dll de MAPI.
  
Los proveedores de servicios pueden contener funciones que no sean MAPI (características completamente no relacionadas con MAPI) en su DLL. Si necesita usar estas características, llame a **LoadLibrary** antes de usar el archivo dll y **FreeLibrary** para quitar la dll de la memoria después de su uso. Debido a que MAPI no reconoce los usos no MAPI de una DLL de proveedor de servicios, no hay ninguna garantía de que el archivo DLL esté disponible cuando sea necesario. MAPI libera una DLL de proveedor de servicios cuando ya no hay clientes con sesiones activas que requieran sus servicios. 
  

