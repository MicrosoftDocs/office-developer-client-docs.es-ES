---
title: RUNADDON (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251492
localization_priority: Normal
ms.assetid: 122c1d30-3cb9-7e7d-b4cc-e93ab8e4da4f
description: Ejecuta un complemento o una macro en un Microsoft proyecto Visual Basic para aplicaciones (VBA).
ms.openlocfilehash: 31ac32c742827311d8aaee4547024ad97d2c48e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19823097"
---
# <a name="runaddon-function"></a>Función RUNADDON

Ejecuta un complemento o una macro en un Microsoft proyecto Visual Basic para aplicaciones (VBA). 
  
## <a name="syntax"></a>Sintaxis

RUNADDON (" *cadena* ") 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _string_ <br/> |Obligatorio  <br/> |**String** <br/> | Nombre de un complemento de la colección **Addons** o de una macro de un proyecto VBA.  <br/> |
   
## <a name="remarks"></a>Comentarios

Si el proyecto del documento que contiene la llamada a la función RUNADDON (u otro proyecto, si se hace referencia a) no tiene una macro (un procedimiento sin argumentos) denominada _cadena_, Microsoft Visio se ejecuta el complemento llamado _cadena_. Si no se encuentra ningún complemento denominado _cadena_ , Visio no realiza ninguna acción y devuelve ningún error. (Puede usar la propiedad **TraceFlags** para supervisar los procedimientos y complementos que intente ejecutar Visio). 
  
Cuando se llama a un procedimiento en un módulo estándar, se recomienda anteponer a la cadena con el nombre del módulo que contiene el procedimiento (por ejemplo, *nombreMódulo.nombreProc*), debido a que más de un módulo puede tener un procedimiento con el mismo nombre. 
  
Para llamar a un procedimiento en un proyecto que no sea el proyecto del documento que contiene la llamada a la función RUNADDON, utilice la sintaxis *nombreProy.nombreMód.nombreProc* (es necesario haber establecido explícitamente una referencia a *projName* en el proyecto de VBA). 
  
> [!NOTE]
>  A partir de Visio 2002, la función RUNADDON no es capaz de ejecutar una cadena que contenga código VBA arbitrario. El código pasado anteriormente a la función RUNADDON se puede mover a un procedimiento de un proyecto VBA de un documento, llamado desde la función RUNADDON. 
  
Para obtener más información acerca de cómo ejecutar código en Visio, vea [Acerca de la configuración de seguridad y la ejecución de código en Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) en esta Referencia de ShapeSheet. 
  
En versiones anteriores de Visio, esta función se denominaba _RUNADDON. La versión 4.0 de Visio y las posteriores aceptan cualquiera de las dos denominaciones. 
  
## <a name="example-1"></a>Ejemplo 1

RUNADDON("Calendar.exe")
  
Inicia un complemento llamado Calendar.exe.
  
## <a name="example-2"></a>Ejemplo 2

RUNADDON("Colocar formas en matriz")
  
Inicia el complemento (implementado por VSL) denominado Colocar formas en matriz.
  
## <a name="example-3"></a>Ejemplo 3

RUNADDON("ThisDocument.ReportStatistics")
  
Llama a la macro ReportStatistics del módulo **ThisDocument** en el proyecto del documento que contiene esta llamada a función. 
  
> [!NOTE]
>  Para invocar una macro del módulo **ThisDocument**, es preciso anteponer "ThisDocument" a la cadena, como muestra el ejemplo. 
  
## <a name="example-4"></a>Ejemplo 4

RUNADDON (" *NombreMódulo* . ReportStatistics") 
  
Llama a la macro ReportStatistics de *NombreMódulo* en el proyecto del documento que contiene esta llamada a función. 
  

