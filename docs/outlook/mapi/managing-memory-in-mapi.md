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
ms.openlocfilehash: c30aa631e70f8f4be52c2fd42dd6bfad900f379e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566162"
---
# <a name="managing-memory-in-mapi"></a>Administración de memoria en MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Sepa cómo y cuándo asignar y liberar memoria es una parte importante de la programación con MAPI. MAPI proporciona funciones tanto las macros que su proveedor de servicio o cliente puede usar para administrar la memoria de una manera coherente. Las tres funciones son los siguientes:
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
Cuando los clientes y proveedores de servicios de usan estas funciones, el problema de "propietario", es decir, sabe cómo liberar: se ha eliminado un bloque de memoria en particular. Un cliente llama a un método de proveedor de servicio no necesita pasar un búfer suficientemente grande para contener un valor devuelto de cualquier tamaño. El proveedor de servicios simplemente puede asignar la cantidad adecuada de memoria mediante **MAPIAllocateBuffer** y, si es necesario, **MAPIAllocateMore**y el cliente pueden más adelante liberarlo a voluntad mediante **MAPIFreeBuffer**, independiente del servicio proveedor. 
  
Las macros de memoria se utilizan para asignar las estructuras o matrices de las estructuras de un tamaño específico. Los clientes y proveedores de servicios deben usar estas macros en lugar de asignar la memoria de forma manual. Por ejemplo, si un cliente necesita para llevar a cabo la resolución de nombres en una lista de destinatarios con tres entradas de procesamiento, se puede utilizar la macro **SizedADRLIST** para crear una estructura **ADRLIST** que se pase a **IAddrBook::ResolveName** con el número correcto de Miembros **ADRENTRY** . Todas las macros de memoria se definen en el MAPIDEFS. Archivo de encabezado H. Estas macros son: 
  
|||
|:-----|:-----|
|[SizedADRLIST](sizedadrlist.md) <br/> |[SizedDtblPage](sizeddtblpage.md) <br/> |
|[SizedDtblButton](sizeddtblbutton.md) <br/> |[SizedENTRYID](sizedentryid.md) <br/> |
|[SizedDtblCheckBox](sizeddtblcheckbox.md) <br/> |[SizedSPropProblemArray](sizedspropproblemarray.md) <br/> |
|[SizedDtblComboBox](sizeddtblcombobox.md) <br/> |[SizedSPropTagArray](sizedsproptagarray.md) <br/> |
|[SizedDtblEdit](sizeddtbledit.md) <br/> |[SizedSRowSet](sizedsrowset.md) <br/> |
|[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |[SizedSSortOrderSet](sizedssortorderset.md) <br/> |
|[SizedDtblLabel](sizeddtbllabel.md) <br/> | <br/> |
   
MAPI también admite el uso de la interfaz [IMalloc](http://msdn.microsoft.com/en-us/library/ms678425%28VS.85%29.aspx) de COM para la administración de memoria. Proveedores de servicios se conceden un puntero de interfaz **IMalloc** por MAPI en la inicialización y también pueden recuperar uno a través de la función [MAPIGetDefaultMalloc](mapigetdefaultmalloc.md) . La principal ventaja de utilizar los métodos **IMalloc** para la administración de memoria a través de las funciones MAPI es que con los métodos COM es posible reasignar un búfer existente. Las funciones de memoria MAPI no admiten la reasignación. 
  

