---
title: HrEntryIDFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrEntryIDFromSz
api_type:
- COM
ms.assetid: 14c171ec-0aec-43ab-8be8-e6bc0ce28a58
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ac59aeb3d650c0fbeb5bcdb580e0401cbab58ee6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437731"
---
# <a name="hrentryidfromsz"></a>HrEntryIDFromSz

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Vuelve a crear un identificador de entrada a partir de su codificación ASCII. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
   
```cpp
HRESULT HrEntryIDFromSz(
  LPSTR sz,
  ULONG FAR * pcb,
  LPENTRYID FAR * ppentry
);
```

## <a name="parameters"></a>Parámetros

 _sz_
  
> [entrada] Puntero a la cadena ASCII desde la que se va a crear un identificador de entrada. 
    
 _indeste_
  
> [salida] Puntero al tamaño, en bytes, del identificador de entrada al que apunta el _parámetro ppentry._ 
    
 _ppentry_
  
> [salida] Puntero a un puntero a la estructura [ENTRYID](entryid.md) devuelta que contiene el nuevo identificador de entrada. 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> La recreación se ha realizado correctamente.
    
MAPI_E_INVALID_ENTRYID
  
> El identificador de entrada no era válido.
    
## <a name="remarks"></a>Comentarios

Las **funciones HrEntryIDFromSz** y [HrSzFromEntryID](hrszfromentryid.md) proporcionan conversión entre la cadena y los formatos binarios de los identificadores de entrada. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

La **función HrEntryIDFromSz** asigna memoria para la cadena ASCII mediante la [función MAPIAllocateBuffer.](mapiallocatebuffer.md) 
  

