---
title: PLAYSOUND (función)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251479
localization_priority: Normal
ms.assetid: 098d216f-e699-0e74-f702-ccfa7809c19b
description: ReProduce un archivo de sonido o un sonido del sistema.
ms.openlocfilehash: 752412aab6584d2b01235fe88644e3ec3fa5daee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346847"
---
# <a name="playsound-function"></a>Función PLAYSOUND

ReProduce un archivo de sonido o un sonido del sistema. 
  
## <a name="syntax"></a>Sintaxis

PlaySound ("* * *filename* * *" | "* * *alias* * *", * * *isAlias* * *, * * *beep* * *, * * *Synch* * *) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Necesario/Opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _largos_ <br/> |Obligatorio  <br/> |**String** <br/> |El nombre del archivo de sonido que desea reproducir.  <br/> |
| _alias_ <br/> |Obligatorio  <br/> |**String** <br/> | Un sonido del sistema representado por un alias.  <br/> |
| _isAlias_ <br/> |Obligatorio  <br/> |**Boolean** <br/> | Especifica si la expresión precedente se trata de un alias o de un nombre de archivo; un valor distinto de cero indica que se trata de un alias.  <br/> |
| _sonora_ <br/> |Obligatorio  <br/> |**Boolean** <br/> |Especifica que Microsoft Visio debe emitir un pitido cuando no se pueda reproducir el sonido seleccionado, para que se oiga el pitido este valor debe ser distinto de cero.  <br/> |
| _sincronización_ <br/> |Obligatorio  <br/> |**Boolean** <br/> |Determina si los sonidos se deben reproducir de forma asincrónica (0) o sincrónica (1).  <br/> |
   
## <a name="remarks"></a>Comentarios

Debe reproducir los sonidos siempre de forma asincrónica para que Visio se pueda seguir ejecutando mientras se reproduce el sonido. Para encadenar varios sonidos de manera que suenen uno a continuación del otro, debe reproducirlos de forma sincrónica ya que, de lo contrario, algunos podrían no reproducirse. 
  
## <a name="example-1"></a>Ejemplo 1

PLAYSOUND("guitarra.wav"; 0; 0; 0)
  
Reproduce el archivo de audio de ondas guitarra.wav de forma asincrónica y sin pitido de advertencia.
  
## <a name="example-2"></a>Ejemplo 2

PLAYSOUND("SystemExclamation", 1, 0, 0)
  
Reproduce el sonido de exclamación de forma asincrónica y sin pitido de advertencia.
  

