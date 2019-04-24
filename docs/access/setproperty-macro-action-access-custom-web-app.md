---
title: DefinirPropiedad (acción de macro) (aplicación web personalizada de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1e97dd95-23f6-4f49-b3b9-2c7261b3a70d
description: Puede usar la acción SetProperty para establecer una propiedad de un control en una vista.
ms.openlocfilehash: 1876be32606d66e0570c9e69206a508b8888b157
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307892"
---
# <a name="setproperty-macro-action-access-custom-web-app"></a>DefinirPropiedad (acción de macro) (aplicación web personalizada de Access)

Puede usar la acción **SetProperty** para establecer una propiedad de un control en una vista. 
  
> [!IMPORTANT]
> Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles. 
  
## <a name="setting"></a>Configuración

La acción **DefinirPropiedad** tiene los argumentos enumerados en la tabla siguiente. 
  
|**Argumento de la acción**|**Descripción**|
|:-----|:-----|
| _Control Name_ <br/> |Escriba el nombre del campo o control para el cual desee definir el valor de una propiedad. Deje este argumento en blanco para establecer la propiedad de la vista.  <br/> |
| _Property_ <br/> |Seleccione la propiedad que desee definir. Vea la sección **Comentarios** de este artículo para ver una lista de las propiedades que se pueden definir mediante esta acción.  <br/> |
| _Value_ <br/> |Escriba el valor en el que desee establecer la propiedad. Para las propiedades cuyos valores son Sí o No, use **-1** para Sí y **0** para No.  <br/> |
   
## <a name="remarks"></a>Comentarios

Puede usar la acción **DefinirPropiedad** para definir las siguientes propiedades de un control: 
  
- Caption
    
- Habilitado
    
- ForeColor
    
- Valor
    
- Visible
    
Si especifica un valor no válido para el argumento ** *Valor* **, no se genera ningún error, pero puede que Access cambie el valor de la propiedad según su interpretación del argumento. 
  

