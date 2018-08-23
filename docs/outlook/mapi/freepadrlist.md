---
title: FreePadrlist
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FreePadrlist
api_type:
- COM
ms.assetid: ca8fbac6-b6f1-46ab-90a1-fc16f0d5824c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 39a184f00ccf54d4fa4477bbdf3086f3e44bddb0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576550"
---
# <a name="freepadrlist"></a>FreePadrlist

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Destruye una estructura de [ADRLIST](adrlist.md) y libera memoria asociada, incluida la memoria asignada para todas las matrices de miembros y estructuras. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
void FreePadrlist(
  LPADRLIST padrlist
);
```

## <a name="parameters"></a>Parámetros

 _padrlist_
  
> [entrada] Puntero a la estructura **ADRLIST** que se va a destruir. 
    
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Como parte de su implementación de **FreePadrlist**, MAPI llama a la función [MAPIFreeBuffer](mapifreebuffer.md) para liberar todas las entradas de la estructura **ADRLIST** antes de liberar la estructura completa. Por lo tanto, deben haber seguido las reglas de asignación para la estructura [ADRLIST](adrlist.md) a todas las entradas de este tipo, con un individuo [MAPIAllocateBuffer](mapiallocatebuffer.md) de llamada para cada matriz de miembros y estructura. 
  
Para obtener más información sobre la asignación de memoria para las estructuras **ADRLIST** y **SRowSet** , vea [Administración de la memoria de ADRLIST y estructuras SRowSet](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI usa el método **FreePadrlist** para liberar una estructura de ADRLIST que se creó para agregar una dirección de uso único a un mensaje.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

