---
title: Función Year (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a70751eb-bfde-4f7d-ad90-a1e4cca25dbc
description: Devuelve un valor numérico que representa el año de la fecha especificada en el calendario gregoriano.
ms.openlocfilehash: 1400c352bcc070035d15b46f8e547e4637364299
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301669"
---
# <a name="year-function-access-custom-web-app"></a>Función Year (aplicación web personalizada de Access)

Devuelve un valor numérico que representa el año de la fecha especificada en el calendario gregoriano.
  
> [!NOTE]
> La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Sintaxis

 **Año** (*Fecha*) 
  
La función **Year** contiene los siguientes argumentos. 
  
|**Nombre de argumento**|**Descripción**|
|:-----|:-----|
| *Date*  <br/> |Una expresión que se puede resolver en un valor Fecha/Hora. La expresión de argumento  *Fecha*  , la expresión de columna, la variable definida por el usuario o el literal de cadena.  <br/> |
   
## <a name="remarks"></a>Comentarios

Los valores devueltos por las funciones **Year**, **Month**y **Day** serán valores gregorianos independientemente del formato de presentación del valor de fecha proporcionado. Por ejemplo, si el formato de presentación de la fecha suministrada utiliza el calendario Hijri, los valores devueltos para las funciones **Year**, **Month**y **Day** serán valores asociados con la fecha Gregoriana equivalente. 
  

