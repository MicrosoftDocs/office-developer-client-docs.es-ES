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
description: Se abre un documento de Microsoft Visio, si no está abierto y activa la ventana de documento.
ms.openlocfilehash: 7d4778fc4641465e88303b8515365172fd8be0ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822696"
---
# <a name="openfile-function"></a>Función OPENFILE

Se abre un documento de Microsoft Visio, si no está abierto y activa la ventana de documento.
  
## <a name="syntax"></a>Sintaxis

 **OPENFILE** ( _"nombre de archivo"_)
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _nombre de archivo_ <br/> |Obligatorio  <br/> |**String** <br/> |El nombre del archivo, incluida la ruta de acceso del archivo que desea abrir.  <br/> |
   
## <a name="remarks"></a>Observaciones

Si hay varias llamadas a la función OPENFILE, se van agregando a una cola y se ejecutan en el orden en que se hayan ido evaluando. Si el documento actual de Visio está activado para modificarlo visualmente, se iniciará una copia nueva de Visio con el nombre de archivo solicitado. 
  
Esta función siempre devuelve el valor FALSE. 
  
En versiones anteriores de la aplicación Visio, esta función se denominaba _OPENFILE. La versión 4.0 de Visio y posteriores aceptan cualquiera de las dos denominaciones. 
  
## <a name="example"></a>Ejemplo

 `OPENFILE("C:/MyFile.vsdx")`
  
Se abre el archivo especificado "MyFile.vsdx" en una ventana nueva o activa la ventana si el archivo ya está abierto. 
  

