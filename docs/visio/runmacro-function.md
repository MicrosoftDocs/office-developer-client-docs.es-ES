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
description: Llama a una macro en un proyecto de Microsoft Visual Basic para Aplicaciones (VBA).
ms.openlocfilehash: 77045bd67fe9be9aab14e73199b33b93c6d70c2c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428091"
---
# <a name="runmacro-function"></a>Función RUNMACRO

Llama a una macro en un proyecto de Microsoft Visual Basic para Aplicaciones (VBA). 
  
## <a name="syntax"></a>Sintaxis

RUNMACRO (** *macroname* ** [, ** *projname_opt* ** ]) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _macroname_ <br/> |Obligatorio  <br/> |**String** <br/> |Nombre de la macro por llamar.  <br/> |
| _projname_opt_ <br/> |Opcional  <br/> |**String** <br/> | Proyecto que contiene la macro.  <br/> |
   
## <a name="remarks"></a>Comentarios

Si se especifica un proyecto, Microsoft Visio examina todos los documentos abiertos para el que  _projname_opt_ y llama a  _macroname_ en ese proyecto. Si  _projname_opt_ se omite o es null (""), se supone que  _macroname_ está en el proyecto VBA del documento que contiene la fórmula RUNMACRO que se está evaluando. 
  
La función RUNMACRO difiere de la función CALLTHIS en que no pasa una referencia a la forma propietaria de la fórmula que se evalúa como  _nombreMacro_. Al igual que CALLTHIS, la función RUNMACRO no requiere una referencia a  _projname_opt_ llamar a ella. 
  
 El código VBA que se invoca cuando una copia de Visio evalúa una función RUNMACRO que forma parte de una fórmula no debe cerrar el documento que contiene la celda que utiliza la función, ya que, de hacerlo, se producirá un error de aplicación y la ejecución de Visio se terminará. 
  
Si necesita cerrar el documento que contiene la celda que usa la función RUNMACRO, puede usar uno de los métodos siguientes:
  
- Cerrar el documento mediante código que no sea de VBA.
    
- Cerrar el documento desde un proyecto diferente al que se cierra.
    
- Enviar mensajes de ventana para cerrar las ventanas del documento en lugar de cerrar el documento.
    
Para obtener más información acerca cómo ejecutar código en Visio, vea [Acerca de la configuración de seguridad y la ejecución de código en Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) en esta Referencia de ShapeSheet. 
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente, se invoca una macro llamada MiPrueba en el módulo de clase ThisDocument del proyecto VBA que contiene la fórmula RUNMACRO. 
  
RUNMACRO ("ThisDocument.MiPrueba") 
  

