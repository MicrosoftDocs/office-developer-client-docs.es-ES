---
title: CONTAINERSHEETREF (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bbdb2dea-4f75-b73e-a98a-0031f34dff2c
description: Devuelve una hoja de referencia al contenedor especificado que contiene la forma.
ms.openlocfilehash: 473d8c0b81ecc568c1d4f3a3b3a885e1ceb4e00d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437269"
---
# <a name="containersheetref-function"></a>Función CONTAINERSHEETREF

Devuelve una hoja de referencia al contenedor especificado que contiene la forma.
  
## <a name="version-information"></a>Información de versión

Versión añadida: Visio 2010
 
  
## <a name="syntax"></a>Sintaxis

CONTAINERSHEETREF(** *index* ** *** [, category]* ** ) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _index_ <br/> |Obligatorio  <br/> |**Integer** <br/> |Índice basado en 1 del contenedor. Para obtener más información, vea los comentarios.  <br/> |
| _category_ <br/> |Opcional  <br/> |**String** <br/> |Categoría del contenedor. Para obtener más información, vea los comentarios.  <br/> |
   
### <a name="return-value"></a>Valor devuelto

Referencia de ShapeSheet
  
## <a name="remarks"></a>Comentarios

El índice de un contenedor se calcula a partir del orden Z de los contenedores, de delante hacia atrás.
  
 *Las*  categorías son cadenas definidas por el usuario que puede usar para clasificar las formas. Las categorías se pueden definir en la celda User.msvShapeCategories, en la ShapeSheet de una forma. Puede definir varias categorías para una forma si las separa con punto y coma. 
  
Si la forma no es miembro de un contenedor o si no hay un contenedor que concuerde tanto con la categoría como con el número de índice especificados, CONTAINERSHEETREF devuelve #REF!.
  
## <a name="example"></a>Ejemplo

CONTAINERSHEETREF(1)! Height 
  
Devuelve el valor de la celda Height del contenedor que se encuentra más hacia delante en la página a la que pertenece la forma. 
  

