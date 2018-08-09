---
title: Función Year (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a70751eb-bfde-4f7d-ad90-a1e4cca25dbc
description: Devuelve un valor numérico que representa el año de la fecha especificada en el calendario gregoriano.
ms.openlocfilehash: f9d72343637734257a2ed9589e5539b845933826
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815518"
---
# <a name="year-function-access-custom-web-app"></a>Función Year (aplicación web personalizado de Access)

Devuelve un valor numérico que representa el año de la fecha especificada en el calendario gregoriano.
  
> [!NOTE]
> La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxis

 **Año** (*Fecha*) 
  
La función **Year** contiene los siguientes argumentos. 
  
|**Nombre del argumento**|**Descripción**|
|:-----|:-----|
| *Date*  <br/> |Una expresión que se puede resolver en un valor Fecha/Hora. La expresión de argumento  *Fecha*  , la expresión de columna, la variable definida por el usuario o el literal de cadena.  <br/> |
   
## <a name="remarks"></a>Comentarios

Los valores devueltos por las funciones **Year**, **Month**y **Day** serán valores de gregoriano independientemente del formato de presentación para el valor de fecha suministrado. Por ejemplo, si el formato de presentación de la fecha proporcionada usa el calendario Hijri, los valores devueltos para el **año**, **mes**y **día** funciones va a ser valores asociados con la fecha del calendario gregoriano equivalente. 
  

