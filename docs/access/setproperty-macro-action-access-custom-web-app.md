---
title: Acción de Macro DefinirPropiedad (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1e97dd95-23f6-4f49-b3b9-2c7261b3a70d
description: Puede usar la acción DefinirPropiedad para establecer una propiedad para un control en una vista.
ms.openlocfilehash: 89ac2b10715d707d3b6ee09ee8ab915384c5acf5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815483"
---
# <a name="setproperty-macro-action-access-custom-web-app"></a>Acción de Macro DefinirPropiedad (aplicación web personalizado de Access)

Puede usar la acción **DefinirPropiedad** para establecer una propiedad para un control en una vista. 
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="setting"></a>Configuración

La acción **DefinirPropiedad** tiene los argumentos enumerados en la siguiente tabla. 
  
|**Argumento de la acción**|**Descripción**|
|:-----|:-----|
| _Control Name_ <br/> |Escriba el nombre del campo o control para el cual desee definir el valor de una propiedad. Deje este argumento en blanco para establecer la propiedad para la vista.  <br/> |
| _Property_ <br/> |Seleccione la propiedad que desee definir. Vea la sección **Comentarios** de este artículo para ver una lista de las propiedades que se pueden definir mediante esta acción.  <br/> |
| _Value_ <br/> |Escriba el valor en el que desee establecer la propiedad. Para las propiedades cuyos valores son Sí o No, use **-1** para Sí y **0** para No.  <br/> |
   
## <a name="remarks"></a>Comentarios

Puede usar la acción **DefinirPropiedad** para definir las siguientes propiedades de un control: 
  
- Caption
    
- Habilitado
    
- ForeColor
    
- Value
    
- Visible
    
Si especifica un valor no válido para el argumento ** *Valor* **, no se genera ningún error, pero puede que Access cambie el valor de la propiedad según su interpretación del argumento. 
  

