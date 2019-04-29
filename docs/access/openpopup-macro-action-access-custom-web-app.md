---
title: Acción de macro OpenPopup (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 850de802-e417-4884-8d14-571de52aa391
description: Abre la vista especificada en una ventana emergente.
ms.openlocfilehash: 2a8b67fcbf31c42f13b36f06d14d9d046be68c68
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427391"
---
# <a name="openpopup-macro-action-access-custom-web-app"></a>Acción de macro OpenPopup (aplicación web personalizada de Access)

Abre la vista especificada en una ventana emergente.
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Sintaxis

 **OpenPopup** (*Ver*, *dónde =*, *ordenar por*) 
  
La acción **OpenPopup** contiene los siguientes argumentos. 
  
|**Nombre de argumento**|**Descripción**|
|:-----|:-----|
| *View*  <br/> |Nombre de la vista que se va a abrir.  <br/> |
| *Donde =*  <br/> |Una cláusula WHERE de SQL válida (sin la palabra WHERE) que restringe los registros de la vista.  <br/> |
| *Ordenar por*  <br/> |Una expresión de cadena que incluye el nombre del campo o campos en los que se van a ordenar los registros y las palabras clave ASC o DESC opcionales. De forma predeterminada, este argumento está en blanco.  <br/> |
   
## <a name="remarks"></a>Comentarios

La macro actual finaliza una vez que se procesa la acción **OpenPopup** . 
  
Las ordenaciones o filtros aplicados por el usuario se borran cuando se llama a la acción **OpenPopup** . 
  
El argumento *OrderBy* es el nombre del campo o campos en los que desea ordenar los registros. Si usa más de un nombre de campo, separe los nombres con una coma (,). 
  
Cuando se establece el argumento *OrderBy* , los registros se ordenan de forma predeterminada en orden ascendente. 
  

