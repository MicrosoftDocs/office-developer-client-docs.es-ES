---
title: Función TimeFromParts (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f631b7e-6e3c-46dc-a05f-6a07f9a91268
description: Devuelve un valor de tiempo en función de elementos especificados.
ms.openlocfilehash: 55a4d1c31fdd2248e3e154d83e803d9f5a5ebb06
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815497"
---
# <a name="timefromparts-function-access-custom-web-app"></a>Función TimeFromParts (aplicación web personalizado de Access)

Devuelve un valor de tiempo en función de elementos especificados.
  
> [!NOTE]
> [!NOTA] La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntax

 **TimeFromParts** (*Hora*, *minuto*, *segundo*) 
  
La función **TimeFromParts** contiene los siguientes argumentos. 
  
|**Nombre del argumento**|**Descripción**|
|:-----|:-----|
| *Hora*  <br/> |Expresión de tipo Integer que especifica horas.  <br/> |
| *Minuto*  <br/> |Expresión de tipo Integer que especifica los minutos.  <br/> |
| *Segundo*  <br/> |Expresión de tipo Integer que especifica los segundos.  <br/> |
   
## <a name="see-also"></a>Ver también

 **TimeFromParts** devuelve un valor de hora totalmente inicializado. Si los argumentos no son válidos, se produce un error. Si cualquiera de los parámetros son null, se devuelve null. 
  

