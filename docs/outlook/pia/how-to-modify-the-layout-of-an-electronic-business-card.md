---
title: Modificar el diseño de una tarjeta de presentación electrónica
TOCTitle: Modify the layout of an electronic business card
ms:assetid: f387c4a7-59c5-4b6a-b33a-1bfa7d499bbf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184653(v=office.15)
ms:contentKeyID: 55119838
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7f85324b31ae865c69e2c40806d9654a0b443f4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320184"
---
# <a name="modify-the-layout-of-an-electronic-business-card"></a>Modificar el diseño de una tarjeta de presentación electrónica

En este ejemplo se muestra cómo modificar el diseño de una tarjeta de presentación electrónica mediante la propiedad [BusinessCardLayoutXml](https://msdn.microsoft.com/library/bb624276\(v=office.15\)) de la interfaz [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)).

## <a name="example"></a>Ejemplo

> [!NOTE] 
> El siguiente ejemplo de código es un fragmento de [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493) (Programación de aplicaciones para Microsoft Office Outlook 2007).

Una tarjeta de presentación electrónica ofrece una vista del contacto que captura información específica de ese contacto. La interfaz **ContactItem** proporciona miembros específicos relacionados con tarjetas de presentación electrónica. Estos miembros son los siguientes: **BusinessCardLayoutXml**, [BusinessCardType](https://msdn.microsoft.com/library/bb612276\(v=office.15\)), [AddBusinessCardLogoPicture(String)](https://msdn.microsoft.com/library/bb646681\(v=office.15\)), [ForwardAsBusinessCard()](https://msdn.microsoft.com/library/bb646342\(v=office.15\)), [ResetBusinessCard()](https://msdn.microsoft.com/library/bb644057\(v=office.15\)), [SaveBusinessCardImage(String)](https://msdn.microsoft.com/library/bb623060\(v=office.15\)) y [ShowBusinessCardEditor()](https://msdn.microsoft.com/library/bb646685\(v=office.15\)).

En el ejemplo de código siguiente, BusinessCardLayoutExample modifica el diseño de una tarjeta de presentación electrónica obteniendo primero un objeto **ContactItem** especificado. En este caso, el objeto **ContactItem** es un contacto en el que el valor de la propiedad [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) es igual a "Melissa MacBeth". Después, BusinessCardLayoutExample crea una clase de documento XML [XmlDocument](https://msdn.microsoft.com/en-us/library/6kza7w4k)y, a continuación, obtiene el atributo de diseño de esta clase en una cadena mediante el valor **BusinessCardLayoutXML** del objeto **ContactItem**. El diseño de la tarjeta se cambia después de alineación a la izquierda a alineación a la derecha.

Si usa Visual Studio para probar este ejemplo de código, primero debe agregar una referencia al componente de la biblioteca de objetos de Microsoft Outlook 15.0 y especificar la variable de Outlook al importar el espacio de nombres **Microsoft.Office.Interop.Outlook**. La instrucción **using** no debe producirse directamente antes de las funciones en el ejemplo de código, pero debe agregarse antes de la declaración de clase pública. La siguiente línea de código muestra cómo llevar a cabo la importación y la asignación en C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void BusinessCardLayoutExample()
{
    Outlook.ContactItem contact =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts).Items.Find(
        "[Subject] = Melissa MacBeth'")
        as Outlook.ContactItem;
    if (contact != null)
    {
        XmlDocument doc = new XmlDocument();
        doc.LoadXml(contact.BusinessCardLayoutXml);
        XmlElement root = doc.DocumentElement;
        string layoutValue = root.GetAttribute("layout");
        if (layoutValue == "left")
        {
            root.SetAttribute("layout", "right");
            contact.BusinessCardLayoutXml = doc.OuterXml;
            contact.Save();
        }
    }
}
```

## <a name="see-also"></a>Vea también

- [Tarjetas de presentación electrónicas](electronic-business-cards.md)

