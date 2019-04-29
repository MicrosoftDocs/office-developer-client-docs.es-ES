---
title: FreeProws
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeProws
api_type:
- HeaderDef
ms.assetid: 0f8f9fc4-4940-4c0a-92cc-2a6409b9a13f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b1109b3201e1b1e4a78c3a0fe0f2eb4d0cd43c05
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438823"
---
# <a name="freeprows"></a>FreeProws

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Destruye una estructura [SRowSet](srowset.md) y libera la memoria asociada, incluida la memoria asignada para todas las matrices y estructuras de miembros. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
void FreeProws(
  LPSRowSet prows
);
```

## <a name="parameters"></a>Parameters

 _prows_
  
> a Puntero a la estructura **SRowSet** que se va a destruir. 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Como parte de su implementación de **FreeProws**, MAPI llama a la función [MAPIFreeBuffer](mapifreebuffer.md) para liberar todas las entradas de la estructura **SRowSet** antes de liberar la estructura completa. Por lo tanto, todas estas entradas deben haber seguido las reglas de asignación para la estructura [SRowSet](srowset.md) , usando una llamada [MAPIAllocateBuffer](mapiallocatebuffer.md) individual para cada matriz y estructura de miembros. 
  
Para obtener más información acerca de la asignación de memoria para las estructuras **ADRLIST** y **SRowSet** , consulte [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI usa el método **FreeProws** para liberar una estructura SRowSet que contiene filas de la tabla que se está procesando.  <br/> |
   
## <a name="see-also"></a>Ver también



[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

