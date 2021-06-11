---
title: FORMPRINTSETUP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FORMPRINTSETUP
api_type:
- COM
ms.assetid: 6e82fe94-47bd-4a25-b25b-0ab6fe2db274
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c2b9176e21341ef28e6f0bc007757b097a05daee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327289"
---
# <a name="formprintsetup"></a>FORMPRINTSETUP

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Describe la información de configuración de impresión del objeto de formulario. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiform.h  <br/> |
   
```cpp
typedef struct
{
  ULONG ulFlags;
  HDEVMODE hDevMode;
  HDEVNAMES hDevNames;
  ULONG ulFirstPageNumber;
  ULONG ulFPrintAttachments;
} FORMPRINTSETUP, FAR * LPFORMPRINTSETUP;

```

## <a name="members"></a>Miembros

 **ulFlags**
  
> Máscara de bits de marcas que controla el tipo de las cadenas. Se puede usar la siguiente marca:
    
MAPI_UNICODE 
  
> Las cadenas están en formato Unicode. Si la MAPI_UNICODE no está establecida, las cadenas tienen el formato ANSI.
    
 **hDevmode**
  
> Controla el modo de la impresora.
    
 **hDevnames**
  
> Controla la ruta de acceso de la impresora.
    
 **ulFirstPageNumber**
  
> Número de página de la primera página que se va a imprimir.
    
 **ulFPrintAttachments**
  
> Marca que indica si hay datos adjuntos que se van a imprimir. Si hay datos adjuntos que imprimir, **el miembro ulFPrintAttachments** se establece en 1. Si no hay datos adjuntos que imprimir, se establece en 0. 
    
## <a name="remarks"></a>Comentarios

La **estructura FORMPRINTSETUP** se usa para describir la información de instalación de impresión de un objeto de formulario. Las implementaciones de [IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md) rellenan la estructura **FORMPRINTSETUP** y la devuelven en el contenido del parámetro de salida  _lppFormPrintSetup_ de **GetPrintSetup**.
  
Si la marca MAPI_UNICODE se pasa en el parámetro  _ulFlags_ de **GetPrintSetup**, las cadenas a las que hacen referencia los miembros **hDevmode** y **hDevnames** deben estar en formato Unicode. De lo contrario, las cadenas deben estar en formato ANSI. 
  
Los visores de formulario que implementan **IMAPIViewContext** deben asignar la estructura **FORMPRINTSETUP** mediante la función de asignador [MAPI MAPIAllocateBuffer](mapiallocatebuffer.md), pero asignar los miembros individuales, **hDevMode** y **hDevNames**, con la función Windows [GlobalAlloc](https://go.microsoft.com/fwlink/?LinkId=132110). La liberación de memoria se controla de forma similar. Los **miembros hDevMode** y **hDevNames** deben liberarse mediante la función Windows [GlobalFree,](https://go.microsoft.com/fwlink/?LinkId=132108) mientras que la estructura **FORMPRINTSETUP** debe liberarse con la función [MAPIFreeBuffer.](mapifreebuffer.md) 
  
## <a name="see-also"></a>Vea también



[IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)


[Estructuras MAPI](mapi-structures.md)

