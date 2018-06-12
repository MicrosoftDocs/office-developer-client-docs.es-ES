---
title: Acción de Macro OpenPopup (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 850de802-e417-4884-8d14-571de52aa391
description: Se abre la vista especificada en una ventana emergente.
ms.openlocfilehash: 01e0086dc0b54837cf5f095ec6ac5701b5b0b219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815460"
---
# <a name="openpopup-macro-action-access-custom-web-app"></a>Acción de Macro OpenPopup (aplicación web personalizado de Access)

Se abre la vista especificada en una ventana emergente.
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="syntax"></a>Syntax

 **OpenPopup** (*Vista*, *donde =*, *Order By*) 
  
La acción **OpenPopup** contiene los siguientes argumentos. 
  
|**Nombre del argumento**|**Descripción**|
|:-----|:-----|
| *View*  <br/> |El nombre de la vista que se va a abrir.  <br/> |
| *Donde =*  <br/> |Una cláusula WHERE de SQL válida (sin la palabra donde) que restringe los registros en la vista.  <br/> |
| *Order By*  <br/> |Una expresión de cadena que incluye el nombre del campo o campos en los que se van a ordenar los registros y las palabras clave ASC o DESC opcionales. De forma predeterminada, este argumento está en blanco.  <br/> |
   
## <a name="remarks"></a>Notas

La macro actual finaliza una vez que se procesa la acción de **OpenPopup** . 
  
Ordenación o los filtros aplicados por el usuario está desactivada cuando se llama a la acción **OpenPopup** . 
  
El argumento *OrderBy* es el nombre del campo o campos en el que desea ordenar los registros. Cuando utilice más de un nombre de campo, separe los nombres con una coma (,). 
  
Cuando se establece el argumento *OrderBy* , los registros se ordenan en orden ascendente de forma predeterminada. 
  

