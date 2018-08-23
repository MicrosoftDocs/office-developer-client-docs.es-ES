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
ms.openlocfilehash: 0686cee9bf6fa47332f75f99e1d2a2d35cb7e7fb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578027"
---
# <a name="freeprows"></a>FreeProws

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Destruye una estructura [SRowSet](srowset.md) y libera memoria asociada, incluida la memoria asignada para todas las matrices de miembros y estructuras. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
void FreeProws(
  LPSRowSet prows
);
```

## <a name="parameters"></a>Parámetros

 _prows_
  
> [entrada] Puntero a la estructura **SRowSet** que se va a destruir. 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Como parte de su implementación de **FreeProws**, MAPI llama a la función [MAPIFreeBuffer](mapifreebuffer.md) para liberar todas las entradas de la estructura de **SRowSet** antes de liberar la estructura completa. Por lo tanto, todas las entradas de esas deben haber seguido las reglas de asignación para la estructura de [SRowSet](srowset.md) , con un individuo [MAPIAllocateBuffer](mapiallocatebuffer.md) de llamada para cada matriz de miembros y estructura. 
  
Para obtener más información sobre la asignación de memoria para las estructuras **ADRLIST** y **SRowSet** , vea [Administración de la memoria de ADRLIST y estructuras SRowSet](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI usa el método **FreeProws** para liberar una estructura SRowSet que contiene las filas de la tabla que se está procesando.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

