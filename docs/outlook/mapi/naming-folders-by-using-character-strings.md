---
title: Asignar nombres a carpetas usando cadenas de caracteres
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec3c023b-7c99-489c-8217-78b303dc10df
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 93d959bf41b5d18610d77c6b5573895b0e3880d4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594589"
---
# <a name="naming-folders-by-using-character-strings"></a><span data-ttu-id="f741c-103">Asignar nombres a carpetas usando cadenas de caracteres</span><span class="sxs-lookup"><span data-stu-id="f741c-103">Naming Folders by Using Character Strings</span></span>

  
  
<span data-ttu-id="f741c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f741c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f741c-105">Si tiene acceso a una o varias carpetas con frecuencia durante una sesión, considere la posibilidad de asignar nombres a las carpetas con el método [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) .</span><span class="sxs-lookup"><span data-stu-id="f741c-105">If you access one or more folders frequently during a session, consider assigning names to the folders with the [IMsgStore::SetReceiveFolder](imsgstore-setreceivefolder.md) method.</span></span> <span data-ttu-id="f741c-106">Aunque **IMsgStore::SetReceiveFolder** se usa principalmente para establecer carpetas especiales para recibir los mensajes entrantes para las clases de mensaje en particular, también se puede usar para asociar cualquier carpeta con un nombre.</span><span class="sxs-lookup"><span data-stu-id="f741c-106">Although **IMsgStore::SetReceiveFolder** is used primarily to establish special folders to receive incoming messages for particular message classes, it can also be used to associate any folder with a name.</span></span> <span data-ttu-id="f741c-107">El nombre puede ser la misma que la clase de mensaje o puede ser cualquier cadena de caracteres, personalizado para el uso de su cliente.</span><span class="sxs-lookup"><span data-stu-id="f741c-107">The name can be the same as the message class or it can be any character string, customized for your client's use.</span></span> <span data-ttu-id="f741c-108">Asociar un nombre a una carpeta, reduce el tiempo necesario para buscar y abrir la carpeta.</span><span class="sxs-lookup"><span data-stu-id="f741c-108">Associating a name with a folder decreases the time it takes to find and open the folder.</span></span> 
  

