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
description: Reproduce un archivo de sonido o un sonido del sistema.
ms.openlocfilehash: ca54b749b764e9ea2c7db71d41268303542417f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19822784"
---
# <a name="playsound-function"></a>Función PLAYSOUND

Reproduce un archivo de sonido o un sonido del sistema. 
  
## <a name="syntax"></a>Sintaxis

PLAYSOUND ("** *filename* **" | "** *alias* **", ** *esAlias* **, ** *beep* **, ** *synch* **) 
  
### <a name="parameters"></a>Parámetros

|**Name**|**Obligatorio/opcional**|**Tipo de datos**|**Descripción**|
|:-----|:-----|:-----|:-----|
| _nombre de archivo_ <br/> |Obligatorio  <br/> |**String** <br/> |El nombre del archivo de sonido que desea reproducir.  <br/> |
| _alias_ <br/> |Obligatorio  <br/> |**String** <br/> | Un sonido del sistema representado por un alias.  <br/> |
| _esAlias_ <br/> |Obligatorio  <br/> |**Boolean** <br/> | Especifica si la expresión precedente se trata de un alias o de un nombre de archivo; un valor distinto de cero indica que se trata de un alias.  <br/> |
| _Bip_ <br/> |Obligatorio  <br/> |**Boolean** <br/> |Especifica que Microsoft Visio debe emitir un pitido cuando no se pueda reproducir el sonido seleccionado, para que se oiga el pitido este valor debe ser distinto de cero.  <br/> |
| _sincronización_ <br/> |Obligatorio  <br/> |**Boolean** <br/> |Determina si los sonidos se deben reproducir de forma asincrónica (0) o sincrónica (1).  <br/> |
   
## <a name="remarks"></a>Observaciones

Debe reproducir los sonidos siempre de forma asincrónica para que Visio se pueda seguir ejecutando mientras se reproduce el sonido. Para encadenar varios sonidos de manera que suenen uno a continuación del otro, debe reproducirlos de forma sincrónica ya que, de lo contrario, algunos podrían no reproducirse.
 
  
## <a name="example-1"></a>Ejemplo 1

PLAYSOUND("guitarra.wav"; 0; 0; 0)
  
Reproduce el archivo de audio de ondas guitarra.wav de forma asincrónica y sin pitido de advertencia.
  
## <a name="example-2"></a>Ejemplo 2

PLAYSOUND("SystemExclamation", 1, 0, 0)
  
Reproduce el sonido de exclamación de forma asincrónica y sin pitido de advertencia.
  

