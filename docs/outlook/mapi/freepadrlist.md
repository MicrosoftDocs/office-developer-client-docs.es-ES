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
ms.openlocfilehash: 2c5d4ec8381d6614cc2bc92fb0a762b068a97a81
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816886"
---
# <a name="freepadrlist"></a>FreePadrlist

  
  
**Hace referencia a**: Outlook 
  
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
   
## <a name="see-also"></a>Vea también



[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

