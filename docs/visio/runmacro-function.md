---
title: RUNMACRO (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033809
localization_priority: Normal
ms.assetid: 86b0f071-5e0b-56de-ff5b-63c114ad823a
description: Llama a una macro de Microsoft Visual Basic para el proyecto de aplicaciones (VBA).
ms.openlocfilehash: e3dd989956ce9c5f795ae3ef0d8535ab2776d6d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823094"
---
# <a name="runmacro-function"></a>RUNMACRO (función)

Llama a una macro de Microsoft Visual Basic para el proyecto de aplicaciones (VBA). 
  
## <a name="syntax"></a>Sintaxis

RUNMACRO (** *macroname* ** [, ** *nombreproy_opc* **]) 
  
### <a name="parameters"></a>Sintaxis

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _macroname_ <br/> |Obligatorio  <br/> |**String** <br/> |Nombre de la macro por llamar.  <br/> |
| _nombreproy_opc_ <br/> |Opcional  <br/> |**String** <br/> | Proyecto que contiene la macro.  <br/> |
   
## <a name="remarks"></a>Observaciones

Si se especifica un proyecto, Microsoft Visio busca en todos los documentos abiertos para el uno que contiene _nombreproy_opc_ y llamadas _macroname_ en ese proyecto. Si _nombreproy_opc_ se omite o es null (""), _macroname_ se supone que en el proyecto de VBA del documento que contiene la fórmula RUNMACRO que se está evaluando. 
  
La función RUNMACRO difiere de la función CALLTHIS en que no pasa una referencia a la forma propietaria de la fórmula que se evalúa para _macroname_. Al igual que CALLTHIS, la función RUNMACRO no requiere una referencia a _nombreproy_opc_ para que llamen a él. 
  
 El código VBA que se invoca cuando una copia de Visio evalúa una función RUNMACRO que forma parte de una fórmula no debe cerrar el documento que contiene la celda que utiliza la función, ya que, de hacerlo, se producirá un error de aplicación y la ejecución de Visio se terminará. 
  
Si necesita cerrar el documento que contiene la celda que usa la función RUNMACRO, puede usar uno de los métodos siguientes:
  
- Cerrar el documento mediante código que no sea de VBA.
    
- Cerrar el documento desde un proyecto diferente al que se cierra.
    
- Enviar mensajes de ventana para cerrar las ventanas del documento en lugar de cerrar el documento.
    
Para obtener más información acerca de cómo ejecutar código en Visio, vea [acerca de la configuración de seguridad y la ejecución de código en Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) en esta referencia de ShapeSheet. 
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente, se invoca una macro llamada MiPrueba en el módulo de clase ThisDocument del proyecto VBA que contiene la fórmula RUNMACRO. 
  
RUNMACRO ("ThisDocument.MiPrueba") 
  

