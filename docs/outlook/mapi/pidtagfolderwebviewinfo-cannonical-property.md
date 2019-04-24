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
ms.openlocfilehash: 70932e703511235e9f5e32efd95b18d1b66494e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316313"
---
# <a name="pidtagfolderwebviewinfo-cannonical-property"></a>Propiedad canónica PidTagFolderWebViewInfo Cannonical Property

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene la dirección URL de la Página principal de una carpeta de Microsoft Outlook. Esta propiedad contiene una secuencia binaria denominada **WebViewPersistenceObject**.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_FOLDER_WEBVIEWINFO  <br/> |
|Identificador:  <br/> |0x36DF  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Carpeta MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Se puede especificar la dirección URL de una página principal para cualquier carpeta de Outlook. Se puede tener acceso a esta información en Outlook desde la ficha **Página principal** del cuadro de diálogo Propiedades de una carpeta. 
  
En función de la configuración de la Directiva, es posible que Outlook omita la Página principal si el almacén MAPI que contiene esta carpeta no informa de MSCAP_SECURE_FOLDER_HOMEPAGES en su implementación de [IMSCapabilities:: GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md) . 
  
Tanto la carpeta **Outlook para hoy** como una carpeta pública pueden tener direcciones URL de la Página principal. Sin embargo, la carpeta **Outlook para hoy** utiliza un mecanismo diferente para administrar la dirección URL de la Página principal; ese mecanismo no se trata en este tema. Una carpeta pública también puede tener definida una dirección URL de la Página principal que sea específica de un usuario. Sin embargo, esta funcionalidad no se describe en este tema. 
  
El valor de esta propiedad es una secuencia binaria llamada **WebViewPersistenceObject**.
  
### <a name="webviewpersistenceobject-stream-structure"></a>Estructura de la secuencia WebViewPersistenceObject

La estructura de la secuencia **WebViewPersistenceObject** contiene información sobre la dirección URL de una página principal de una carpeta. 
  
Los elementos de datos de esta estructura se almacenan en el orden de bytes Little-endian, inmediatamente uno tras otro en el orden especificado. 
  
> [!NOTE]
> La siguiente descripción puede no mostrar todos los valores de campo compatibles con Outlook; por lo tanto, cuando el código Lee una secuencia existente, es posible que también se encuentren algunas marcas que no se muestran aquí. Sin embargo, puede usar esta descripción para crear mediante programación valores de la propiedad **PidTagFolderWebViewInfo** que Outlook entiende. 
  
 _dwVersion_
  
> DWORD (4 bytes). La versión del formato de la estructura. A partir de Microsoft Office Outlook 2007, el único valor admitido para este campo es el siguiente.
    
|**Nombre del valor**|**Value**|
|:-----|:-----|
|WEBVIEW_PERSISTENCE_VERSION  <br/> |0x00000002  <br/> |
   
 _dwType_
  
> DWORD (4 bytes). Tipo de información de la Página principal. A partir de Microsoft Office Outlook 2007, el único valor admitido para este campo es el siguiente.
    
|**Nombre del valor**|**Value**|
|:-----|:-----|
|WEBVIEWURL  <br/> |0x00000001  <br/> |
   
 _dwFlags_
  
> DWORD (4 bytes). Una combinación de cero o más indicadores cuyos valores y significados se enumeran en la tabla siguiente.
    
|Nombre de marca * * * *|****Valor****|****Descripción****|
|:-----|:-----|:-----|
|WEBVIEW_FLAGS_SHOWBYDEFAULT  <br/> |0x00000001  <br/> |La casilla de verificación **Mostrar Página principal de forma predeterminada para esta carpeta** se activaba en la ficha **Página principal** del cuadro de diálogo Propiedades de una carpeta.  <br/> |
   
 _dwUnused [7]_
  
> Una matriz de 7 elementos DWORD (total de 28 bytes). Sin usar.
    
cbData
  
> Un ULONG (4 bytes). Tamaño, en bytes, del elemento de datos _wzURL_ . 
    
 _wzURL_
  
> Una matriz de elementos WCHAR. Representación UTF-16 de la cadena de la dirección URL de la Página principal terminada en cero.
    
### <a name="webviewpersistenceobject-stream-sample"></a>Ejemplo de secuencia WebViewPersistenceObject

En esta sección se describe un ejemplo de una secuencia **WebViewPersistenceObject** . La secuencia especifica la dirección URL de lahttps://www.microsoft.comPágina principal "". 
  
 **Volcado de datos**
  
El siguiente es un volcado de datos de la secuencia tal como se mostraría en un editor binario.
  
|**Desplazamiento de secuencia**|**Bytes de datos**|**Datos ASCII**|
|:-----|:-----|:-----|
|0000000000  <br/> | `02 00 00 00 01 00 00 00 01 00 00 00 00 00 00 00` <br/> | `?...?...?.......` <br/> |
|0000000010  <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
|0000000020  <br/> | `00 00 00 00 00 00 00 00 32 00 00 00 68 00 74 00` <br/> | `........2...h.t.` <br/> |
|0000000030  <br/> | `74 00 70 00 3A 00 2F 00 2F 00 77 00 77 00 77 00` <br/> | `t.p.:././.w.w.w.` <br/> |
|0000000040  <br/> | `2E 00 6D 00 69 00 63 00 72 00 6F 00 73 00 6F 00` <br/> | `..m.i.c.r.o.s.o.` <br/> |
|0000000050  <br/> | `66 00 74 00 2E 00 63 00 6F 00 6D 00 00 00` <br/> | `f.t...c.o.m...` <br/> |
   
A continuación se muestra un análisis de los datos de ejemplo para la secuencia **WebViewPersistenceObject** . 
  
 _dwVersion_
  
> Offset 0X0, 4 bytes: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).
    
 _dwType_
  
> Desplazamiento 0x4, 4 bytes: 0x00000001 (WEBVIEWURL).
    
 _dwFlags_
  
> Desplazamiento 0x8, 4 bytes: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).
    
 _dwUnused [7]_
  
> PosiciónInicial 0xC, 28 bytes: todo ceros.
    
 _cbData_
  
> Desplazamiento 0x28, 4 bytes: 0x00000032.
    
 _wzURL_
  
> Desplazamiento 0x2C bytes: matriz de 25 WCHARs. Un valor de cadena terminada en cero Unicodehttps://www.microsoft.com: "".
    

