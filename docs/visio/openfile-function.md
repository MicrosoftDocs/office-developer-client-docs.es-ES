---
title: OPENFILE (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251471
localization_priority: Normal
ms.assetid: ff59ab04-a589-cf9e-db3b-20658a7dffdc
description: Abre un documento Visio microsoft, si aún no está abierto, y activa la ventana del documento.
ms.openlocfilehash: 5a89a658e560d144007ec19796de82b9949bea82
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419579"
---
# <a name="openfile-function"></a>Función OPENFILE

Abre un documento Visio microsoft, si aún no está abierto, y activa la ventana del documento.
  
## <a name="syntax"></a>Sintaxis

 **OPENFILE**( _"filename"_)
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _filename_ <br/> |Obligatorio  <br/> |**String** <br/> |Nombre del archivo, incluida la ruta de acceso de archivo, que desea abrir.  <br/> |
   
## <a name="remarks"></a>Comentarios

Si hay varias llamadas a la función OPENFILE, se van agregando a una cola y se ejecutan en el orden en que se hayan ido evaluando. Si el documento actual de Visio está activado para modificarlo visualmente, se iniciará una copia nueva de Visio con el nombre de archivo solicitado. 
  
Esta función siempre devuelve el valor FALSE. 
  
En versiones anteriores de la aplicación Visio, esta función se denominaba _OPENFILE. La versión 4.0 de Visio y posteriores aceptan cualquiera de las dos denominaciones. 
  
## <a name="example"></a>Ejemplo

 `OPENFILE("C:/MyFile.vsdx")`
  
Abre el archivo especificado "MyFile.vsdx" en una nueva ventana o activa la ventana si el archivo ya está abierto. 
  

