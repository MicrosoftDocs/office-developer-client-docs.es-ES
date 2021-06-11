---
title: Administración de memoria en MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9eee6925-ab91-413e-8907-c747ab4a4bb5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 66489c09be641d8fe9ae5f3ffff46a6d5004f473
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298099"
---
# <a name="managing-memory-in-mapi"></a>Administración de memoria en MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Saber cómo y cuándo asignar y liberar memoria es una parte importante de la programación con MAPI. MAPI proporciona funciones y macros que el cliente o el proveedor de servicios pueden usar para administrar la memoria de forma coherente. Las tres funciones son las siguientes:
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
Cuando los clientes y los proveedores de servicios usan estas funciones, se elimina el problema de quién "posee" (es decir, sabe cómo liberar) un bloque determinado de memoria. Un cliente que llama a un método de proveedor de servicios no necesita pasar un búfer lo suficientemente grande como para contener un valor devuelto de cualquier tamaño. El proveedor de servicios simplemente puede asignar la cantidad adecuada de memoria mediante **MAPIAllocateBuffer** y, si es necesario, **MAPIAllocateMore**, y el cliente puede liberarla posteriormente a voluntad usando **MAPIFreeBuffer**, independientemente del proveedor de servicios. 
  
Las macros de memoria se usan para asignar estructuras o matrices de estructuras de un tamaño específico. Los clientes y proveedores de servicios deben usar estas macros en lugar de asignar la memoria manualmente. Por ejemplo, si un cliente necesita realizar el procesamiento de resolución de nombres en una lista de destinatarios con tres entradas, la macro **SizedADRLIST** se puede usar para crear una estructura **ADRLIST** para pasar a **IAddrBook::ResolveName** con el número correcto de miembros **adrentry.** Todas las macros de memoria se definen en MAPIDEFS. Archivo de encabezado H. Estas macros son: 
  
|||
|:-----|:-----|
|[SizedADRLIST](sizedadrlist.md) <br/> |[SizedDtblPage](sizeddtblpage.md) <br/> |
|[SizedDtblButton](sizeddtblbutton.md) <br/> |[SizedENTRYID](sizedentryid.md) <br/> |
|[SizedDtblCheckBox](sizeddtblcheckbox.md) <br/> |[SizedSPropProblemArray](sizedspropproblemarray.md) <br/> |
|[SizedDtblComboBox](sizeddtblcombobox.md) <br/> |[SizedSPropTagArray](sizedsproptagarray.md) <br/> |
|[SizedDtblEdit](sizeddtbledit.md) <br/> |[SizedSRowSet](sizedsrowset.md) <br/> |
|[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |[SizedSSortOrderSet](sizedssortorderset.md) <br/> |
|[SizedDtblLabel](sizeddtbllabel.md) <br/> | <br/> |
   
MAPI también admite el uso de la interfaz COM [IMalloc para](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx) la administración de memoria. MAPI proporciona a los proveedores de servicios un puntero de interfaz **IMalloc** en el momento de la inicialización y también puede recuperar uno a través de la [función MAPIGetDefaultMalloc.](mapigetdefaultmalloc.md) La principal ventaja de usar los métodos **IMalloc** para administrar la memoria a través de las funciones MAPI es que con los métodos COM es posible reasignar un búfer existente. Las funciones de memoria MAPI no admiten la reasignación. 
  

