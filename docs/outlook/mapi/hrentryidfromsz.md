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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347813"
---
# <a name="hrentryidfromsz"></a>HrEntryIDFromSz

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Vuelve a crear un identificador de entrada a partir de su codificación ASCII. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
   
```cpp
HRESULT HrEntryIDFromSz(
  LPSTR sz,
  ULONG FAR * pcb,
  LPENTRYID FAR * ppentry
);
```

## <a name="parameters"></a>Parameters

 _SZ_
  
> a Puntero a la cadena ASCII a partir de la cual se va a crear un identificador de entrada. 
    
 _impreso_
  
> contempla Puntero al tamaño, en bytes, del identificador de entrada al que apunta el parámetro _ppentry_ . 
    
 _ppentry_
  
> contempla Puntero a un puntero a la estructura [EntryID](entryid.md) devuelta que contiene el nuevo identificador de entrada. 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> El recreo se realizó correctamente.
    
MAPI_E_INVALID_ENTRYID
  
> El identificador de entrada no era válido.
    
## <a name="remarks"></a>Comentarios

Las funciones **HrEntryIDFromSz** y [HrSzFromEntryID](hrszfromentryid.md) proporcionan conversión entre los formatos binarios y de cadena de los identificadores de entrada. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

La función **HrEntryIDFromSz** asigna memoria para la cadena ASCII mediante la función [MAPIAllocateBuffer](mapiallocatebuffer.md) . 
  

