---
title: Propiedad DBEngine.DefaultPassword (DAO)
TOCTitle: DefaultPassword Property
ms:assetid: 189e34f3-d573-c75f-8be2-d98c50df8a52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845616(v=office.15)
ms:contentKeyID: 48543478
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 72e73d29129c749d5479e2c7b17827f13adb4847
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704738"
---
# <a name="dbenginedefaultpassword-property-dao"></a><span data-ttu-id="16b52-102">Propiedad DBEngine.DefaultPassword (DAO)</span><span class="sxs-lookup"><span data-stu-id="16b52-102">DBEngine.DefaultPassword property (DAO)</span></span>


<span data-ttu-id="16b52-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="16b52-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="16b52-p101">Establece la contraseña utilizada para crear el objeto **Workspace** predeterminado cuando se inicializa. **String** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="16b52-p101">Sets the password used to create the default **Workspace** when it is initialized. Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="16b52-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="16b52-106">Syntax</span></span>

<span data-ttu-id="16b52-107">*expresión* . DefaultPassword</span><span class="sxs-lookup"><span data-stu-id="16b52-107">*expression* .DefaultPassword</span></span>

<span data-ttu-id="16b52-108">*expresión* Variable que representa un objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="16b52-108">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="16b52-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="16b52-109">Remarks</span></span>

<span data-ttu-id="16b52-p102">El valor de **DefaultPassword** es un tipo de datos String que puede tener una longitud de hasta 20 caracteres. Puede contener cualquier carácter excepto ASCII 0.</span><span class="sxs-lookup"><span data-stu-id="16b52-p102">The setting for **DefaultPassword** is a String data type that can be up to 20 characters long. It can contain any character except ASCII 0.</span></span>


> [!NOTE]
> <span data-ttu-id="16b52-p103">[!NOTA] Use contraseñas seguras que combinen letras mayúsculas y minúsculas, números y símbolos. Las contraseñas que no son seguras no contienen una combinación de estos elementos. Contraseña segura: Y6dh!et5. Contraseña no segura: House27. Use una contraseña segura que pueda recordar para no tener que anotarla.</span><span class="sxs-lookup"><span data-stu-id="16b52-p103">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span>

<span data-ttu-id="16b52-117">De forma predeterminada, la propiedad **DefaultUser** está establecida en "admin" y la propiedad **DefaultPassword** está establecida en una cadena de longitud cero ("").</span><span class="sxs-lookup"><span data-stu-id="16b52-117">By default, the **DefaultUser** property is set to "admin" and the **DefaultPassword** property is set to a zero-length string ("").</span></span>

<span data-ttu-id="16b52-p104">En general, se utiliza el método **CreateWorkspace** para crear un objeto **Workspace** con un nombre de usuario y una contraseña determinados. Sin embargo, por compatibilidad con versiones anteriores y por comodidad cuando no se implementa una base de datos protegida, el motor de base de datos de Microsoft Access crea automáticamente un objeto **Workspace** predeterminado cuando es necesario si no hay uno abierto. En este caso, los valores de las propiedades **DefaultUser** y **DefaultPassword** definen el nombre de usuario y la contraseña para el objeto **Workspace** predeterminado.</span><span class="sxs-lookup"><span data-stu-id="16b52-p104">Typically, you use the **CreateWorkspace** method to create a **Workspace** object with a given user name and password. However, for backward compatibility with earlier versions and for convenience when you don't implement a secured database, the Microsoft Access database engine automatically creates a default **Workspace** object when needed if one isn't already open. In this case, the **DefaultUser** and **DefaultPassword** property values define the user and password for the default **Workspace** object.</span></span>

<span data-ttu-id="16b52-121">Para que esta propiedad surta efecto, debe establecerla antes de llamar a los métodos DAO.</span><span class="sxs-lookup"><span data-stu-id="16b52-121">For this property to take effect, you should set it before calling any DAO methods.</span></span>

