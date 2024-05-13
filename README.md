# DecryptInterviewQuestion
using System;

class Program
{
    static void Main(string[] args)
    {
        string input = "olleH I epoh uoy era gniod llew";
        string output = ReverseWordsAndFixSpaces(input);
        Console.WriteLine(output);
    }

    static string ReverseWordsAndFixSpaces(string input)
    {
        // Split the input string into words
        string[] words = input.Split(new char[] { ' ' }, StringSplitOptions.RemoveEmptyEntries);

        // Reverse each word and join them with a single space
        string reversedSentence = string.Join(" ", Array.ConvertAll<string, string>(words, ReverseString));

        return reversedSentence;
    }

    static string ReverseString(string input)
    {
        char[] charArray = input.ToCharArray();
        Array.Reverse(charArray);
        return new string(charArray);
    }
}
