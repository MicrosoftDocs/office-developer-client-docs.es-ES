---
title: Propiedad DBEngine.DefaultUser (DAO)
TOCTitle: DefaultUser Property
ms:assetid: 41ee0211-0794-6026-7341-3698a0b2c588
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192905(v=office.15)
ms:contentKeyID: 48544464
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053071
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c29f9663ce3591fe5b1633239e8ec0d8866ee16a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717541"
---
# <a name="dbenginedefaultuser-property-dao"></a><span data-ttu-id="44625-102">Propiedad DBEngine.DefaultUser (DAO)</span><span class="sxs-lookup"><span data-stu-id="44625-102">DBEngine.DefaultUser property (DAO)</span></span>


<span data-ttu-id="44625-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="44625-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="44625-p101">Establece el nombre de usuario utilizado para crear el objeto **Workspace** predeterminado cuando se inicializa. **String** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="44625-p101">Sets the user name used to create the default **Workspace** when it is initialized. Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="44625-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44625-106">Syntax</span></span>

<span data-ttu-id="44625-107">*expresión* . DefaultUser</span><span class="sxs-lookup"><span data-stu-id="44625-107">*expression* .DefaultUser</span></span>

<span data-ttu-id="44625-108">*expresión* Una expresión que devuelve un objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="44625-108">*expression* An expression that returns a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="44625-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="44625-109">Remarks</span></span>

<span data-ttu-id="44625-110">El valor de **DefaultUser** es un tipo de datos String.</span><span class="sxs-lookup"><span data-stu-id="44625-110">The setting for **DefaultUser** is a String data type.</span></span> <span data-ttu-id="44625-111">Puede ser 1 y 20 caracteres largos en Microsoft Access áreas de trabajo y pueden incluir caracteres alfabéticos, caracteres acentuados, números, espacios y símbolos excepto: "(comillas), / (barra diagonal), \\ (barra diagonal inversa), \[ \] (corchetes) ,: (dos puntos), | (barra vertical), \< (menos-de inicio de sesión), \> (mayor-de inicio de sesión), + (signo más), = (signo igual), ¿(punto y coma), (coma),?</span><span class="sxs-lookup"><span data-stu-id="44625-111">It can be 1–20 characters long in Microsoft Access workspaces and it can include alphabetic characters, accented characters, numbers, spaces, and symbols except for: " (quotation marks), / (forward slash), \\ (backslash), \[ \] (brackets), : (colon), | (pipe), \< (less-than sign), \> (greater-than sign), + (plus sign), = (equal sign), ; (semicolon), , ( comma), ?</span></span> <span data-ttu-id="44625-112">(signo de interrogación), \* (asterisco), espacios y caracteres de control (ASCII 00 hasta ASCII 31) líderes.</span><span class="sxs-lookup"><span data-stu-id="44625-112">(question mark), \* (asterisk), leading spaces, and control characters (ASCII 00 to ASCII 31).</span></span>


> [!NOTE]
> <span data-ttu-id="44625-p103">[!NOTA] Use contraseñas seguras que combinen letras mayúsculas y minúsculas, números y símbolos. Las contraseñas que no son seguras no contienen una combinación de estos elementos. Contraseña segura: Y6dh!et5. Contraseña no segura: House27. Use una contraseña segura que pueda recordar para no tener que anotarla.</span><span class="sxs-lookup"><span data-stu-id="44625-p103">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span>

<span data-ttu-id="44625-118">De forma predeterminada, la propiedad **DefaultUser** está establecida en "admin" y la propiedad **DefaultPassword** está establecida en una cadena de longitud cero ("").</span><span class="sxs-lookup"><span data-stu-id="44625-118">By default, the **DefaultUser** property is set to "admin" and the **DefaultPassword** property is set to a zero-length string ("").</span></span>

<span data-ttu-id="44625-p104">Los nombres de usuario no suelen distinguir entre mayúsculas y minúsculas; sin embargo, si va a volver a crear una cuenta de usuario que se ha eliminado o creado en un grupo de trabajo diferente, el nombre de usuario debe coincidir exactamente en las mayúsculas y minúsculas con el nombre original. Las contraseñas sí distinguen entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="44625-p104">User names aren't usually case-sensitive; however, if you're re-creating a user account that was deleted or created in a different workgroup, the user name must be an exact case-sensitive match of the original name. Passwords are case-sensitive.</span></span>

<span data-ttu-id="44625-p105">En general, se utiliza el método **CreateWorkspace** para crear un objeto **Workspace** con un nombre de usuario y una contraseña determinados. Sin embargo, por compatibilidad con versiones anteriores y por comodidad cuando no se implementa una base de datos protegida, el motor de base de datos de Microsoft Access crea automáticamente un objeto **Workspace** predeterminado cuando es necesario si no hay uno abierto. En este caso, los valores de las propiedades **DefaultUser** y **DefaultPassword** definen el nombre de usuario y la contraseña para el objeto **Workspace** predeterminado.</span><span class="sxs-lookup"><span data-stu-id="44625-p105">Typically, you use the **CreateWorkspace** method to create a **Workspace** object with a given user name and password. However, for backward compatibility with earlier versions and for convenience when you don't implement a secured database, the Microsoft Access database engine automatically creates a default **Workspace** object when needed if one isn't already open. In this case, the **DefaultUser** and **DefaultPassword** property values define the user and password for the default **Workspace** object.</span></span>

<span data-ttu-id="44625-124">Para que esta propiedad surta efecto, debe establecerla antes de llamar a los métodos DAO.</span><span class="sxs-lookup"><span data-stu-id="44625-124">For this property to take effect, you should set it before calling any DAO methods.</span></span>

