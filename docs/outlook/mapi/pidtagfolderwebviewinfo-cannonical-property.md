---
title: Propiedad canónica PidTagFolderWebViewInfo Cannonical Property
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderWebViewInfo
api_type:
- HeaderDef
ms.assetid: 96ea23df-aa4f-4b3e-9663-e7db39f668c1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 62bc0e75d0a405ebe9f68ec9f4af1ca038bda219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819531"
---
# <a name="pidtagfolderwebviewinfo-cannonical-property"></a>Propiedad canónica PidTagFolderWebViewInfo Cannonical Property

  
  
**Hace referencia a**: Outlook 
  
Contiene la dirección URL de la página principal de una carpeta de Microsoft Outlook. Esta propiedad contiene una secuencia binaria denominada **WebViewPersistenceObject**.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_FOLDER_WEBVIEWINFO  <br/> |
|Identificador:  <br/> |0x36DF  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Carpeta MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Para cualquier carpeta de Outlook, se puede especificar una dirección URL de la página principal. Esta información se puede acceder en Outlook desde la ficha **página principal** del cuadro de diálogo Propiedades de una carpeta. 
  
Dependiendo de determinadas opciones de directiva, si el almacén MAPI que contiene esta carpeta no informa MSCAP_SECURE_FOLDER_HOMEPAGES en su implementación de [IMSCapabilities::GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md) se puede omitir la página principal de Outlook. 
  
La carpeta de **Outlook para hoy** y una carpeta pública pueden tener direcciones URL de la página principal. Sin embargo la carpeta de **Outlook para hoy** utiliza un mecanismo diferente para administrar su dirección URL de la página principal; Este mecanismo no se aborda en este tema. Una carpeta pública también podría tener una dirección URL de página principal definida en lo que es específica de un usuario. Sin embargo, esta capacidad no se describe en este tema. 
  
El valor de esta propiedad es una secuencia binaria denominada **WebViewPersistenceObject**.
  
### <a name="webviewpersistenceobject-stream-structure"></a>Estructura de la secuencia de WebViewPersistenceObject

La estructura de la secuencia de **WebViewPersistenceObject** contiene información sobre una dirección URL de la página principal de una carpeta. 
  
Elementos de datos de esta estructura se almacenan en orden de bytes little-endian, inmediatamente después de unos a otros en el siguiente orden especificado. 
  
> [!NOTE]
> La siguiente descripción no puede enumerar todos los valores de campo compatibles con Outlook; por lo tanto, cuando el código lee una secuencia existente, es posible que también se puede encontrar algunas marcas que no se muestran aquí. Sin embargo, puede usar esta descripción para crear mediante programación los valores de la propiedad **PidTagFolderWebViewInfo** que Outlook sabrá. 
  
 _dwVersion_
  
> DWORD (4 bytes). La versión del formato de la estructura. A partir de Microsoft Office Outlook 2007, el único valor admitido para este campo es el siguiente.
    
|**Nombre del valor**|**Valor**|
|:-----|:-----|
|WEBVIEW_PERSISTENCE_VERSION  <br/> |0x00000002  <br/> |
   
 _dwType_
  
> DWORD (4 bytes). El tipo de la información de la página principal. A partir de Microsoft Office Outlook 2007, el único valor admitido para este campo es el siguiente.
    
|**Nombre del valor**|**Valor**|
|:-----|:-----|
|WEBVIEWURL  <br/> |0x00000001  <br/> |
   
 _dwFlags_
  
> DWORD (4 bytes). Una combinación de cero o más indicadores cuyos valores y significados se enumeran en la siguiente tabla.
    
|Nombre de marca ***|****Valor****|****Descripción****|
|:-----|:-----|:-----|
|WEBVIEW_FLAGS_SHOWBYDEFAULT  <br/> |0x00000001  <br/> |En la ficha **página principal** del cuadro de diálogo Propiedades de una carpeta que se protegió la casilla de verificación **Mostrar página principal de forma predeterminada para esta carpeta** .  <br/> |
   
 _dwUnused [7]_
  
> Una matriz de elementos DWORD 7 (total de 28 bytes). No se utiliza.
    
cbData
  
> ULONG (4 bytes). El tamaño, en bytes, del elemento de datos de _wzURL_ . 
    
 _wzURL_
  
> Una matriz de elementos WCHAR. La representación UTF-16 de la cadena de dirección URL terminada en cero de la página principal.
    
### <a name="webviewpersistenceobject-stream-sample"></a>Ejemplo de secuencia de WebViewPersistenceObject

En esta sección se describe un ejemplo de una secuencia de **WebViewPersistenceObject** . La secuencia especifica la dirección URL de la página principal "http://www.microsoft.com". 
  
 **Volcado de datos**
  
El siguiente es un volcado de datos de la secuencia tal y como se mostrarían en un editor binario.
  
|**Desplazamiento de la secuencia**|**Bytes de datos**|**Datos ASCII**|
|:-----|:-----|:-----|
|0000000000  <br/> | `02 00 00 00 01 00 00 00 01 00 00 00 00 00 00 00` <br/> | `?...?...?.......` <br/> |
|0000000010  <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
|0000000020  <br/> | `00 00 00 00 00 00 00 00 32 00 00 00 68 00 74 00` <br/> | `........2...h.t.` <br/> |
|0000000030  <br/> | `74 00 70 00 3A 00 2F 00 2F 00 77 00 77 00 77 00` <br/> | `t.p.:././.w.w.w.` <br/> |
|0000000040  <br/> | `2E 00 6D 00 69 00 63 00 72 00 6F 00 73 00 6F 00` <br/> | `..m.i.c.r.o.s.o.` <br/> |
|0000000050  <br/> | `66 00 74 00 2E 00 63 00 6F 00 6D 00 00 00` <br/> | `f.t...c.o.m...` <br/> |
   
El siguiente es un análisis de los datos de ejemplo de la secuencia de **WebViewPersistenceObject** . 
  
 _dwVersion_
  
> Desplazamiento 0 x 0, 4 bytes: 0 x 00000002 (WEBVIEW_PERSISTENCE_VERSION).
    
 _dwType_
  
> Desplazamiento 0 x 4, 4 bytes: 0 x 00000001 (WEBVIEWURL).
    
 _dwFlags_
  
> Desplazamiento 0 x 8, 4 bytes: 0 x 00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).
    
 _dwUnused [7]_
  
> Desplazamiento 0xC, 28 bytes: todos los ceros.
    
 _cbData_
  
> Desplazamiento 0 x 28, 4 bytes: 0 x 00000032.
    
 _wzURL_
  
> Desplazamiento 0x2C, 0 x 32 bytes: matriz de número de 25 WCHAR. Un valor de cadena terminada en cero de Unicode: "http://www.microsoft.com".
    

